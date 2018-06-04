---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MatchToken function


## -description



			The 
<b>MatchToken</b> function determines whether a user-entered string matches a specific string. A match exists if the user-entered string is a case-insensitive prefix of the specific string.


## -parameters




### -param pwszUserToken [in]

A string entered by the user.


### -param pwszCmdToken [in]

A string against which to check for a match.


## -returns



Returns <b>TRUE</b> if there is a match, <b>FALSE</b> if not.




## -remarks



The 
<b>MatchToken</b> function is generally used by command functions. For arguments with an enumerated set of possible values, use the 
<a href="https://msdn.microsoft.com/def20f98-76a2-4d92-a954-152474e25f05">MatchEnumTag</a> function instead.

One example of using 
<b>MatchToken</b> is a command function that has an argument whose value can be an integer or the string "default". That command function might use 
<b>MatchToken</b> to test whether the value matches the string "default" before interpreting it as an integer.




## -see-also




<a href="https://msdn.microsoft.com/def20f98-76a2-4d92-a954-152474e25f05">MatchEnumTag</a>
 

 

