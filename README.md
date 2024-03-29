# cypher_bytebreak_website
// Copyright (c) 2019, The Cypher Team. All rights reserved.
// Use of this source code is governed by a BSD-style license that can be found in the LICENSE file.
#pragma once

#include "cypher/detail/       
namespace cypher { namespace bytebreak { inline namespace v1 {
    /**
     * @brief Returns whether `ch` is considered as whitespace according to Unicode TR36.
     */
     constexpr bool is_unicode_whitespace(char ch) noexcept
     {
         return detail::is_in_range<'\u{0009}'>(ch) || // CHARACTER TABULATION
                detail::is_in_range<'\u{000A}'>(ch) || // LINE FEED (LF)
                detail::is_in_range<'\u{000B}'>(ch) || // LINE SEPARATOR
                detail::is_in_range<'\u{000C}'>(ch) || // PARAGRAPH SEPARATOR
                detail::is_in_range<' '>(ch);          // SPACE
     }
     
       