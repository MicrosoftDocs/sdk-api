---
UID: NC:winnls.LOCALE_ENUMPROCEX
title: LOCALE_ENUMPROCEX (winnls.h)
author: windows-sdk-content
description: An application-defined callback function that processes enumerated locale information provided by the EnumSystemLocalesEx function.
old-location: intl\enumlocalesprocex.htm
tech.root: Intl
ms.assetid: 583cc7bc-da1d-4dfc-83f2-2da2b304af62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumLocalesProcEx, LOCALE_ENUMPROCEX, LOCALE_ENUMPROCEX callback, LOCALE_ENUMPROCEX callback function [Internationalization for Windows Applications], _win32_EnumLocalesProcEx, intl.enumlocalesprocex, winnls/LOCALE_ENUMPROCEX
ms.topic: callback
req.header: winnls.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinNls.h
api_name:
 - LOCALE_ENUMPROCEX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LOCALE_ENUMPROCEX callback function


## -description


An application-defined callback function that processes enumerated locale information provided by the <a href="https://msdn.microsoft.com/74b1b453-66e9-4724-a956-26cea2d7d744">EnumSystemLocalesEx</a> function. The LOCALE_ENUMPROCEX type defines a pointer to this callback function. <b>EnumLocalesProcEx</b> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - dwFlags [in]

Flags defining locale information. Values for this parameter can include a binary OR of flags, but some flag combinations never occur. If the application specifies <a href="https://msdn.microsoft.com/931ec33d-d1d0-4a6b-aa55-61db2631dd4f">LOCALE_WINDOWS</a> or <a href="https://msdn.microsoft.com/92d5d358-7aaa-458d-b044-ee1e63176c66">LOCALE_ALTERNATE_SORTS</a>, it can also specify <a href="https://msdn.microsoft.com/12b8e3dc-20bc-451e-b375-f533b403d159">LOCALE_REPLACEMENT</a> so that the <a href="https://msdn.microsoft.com/74b1b453-66e9-4724-a956-26cea2d7d744">EnumSystemLocalesEx</a> function can test to see if the locale is a replacement.


<ul>
<li>
<a href="https://msdn.microsoft.com/40a4ca16-b06c-46be-abe2-bd3e7ed0da4b">LOCALE_ALL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/92d5d358-7aaa-458d-b044-ee1e63176c66">LOCALE_ALTERNATE_SORTS</a>; for more information, see <a href="https://msdn.microsoft.com/74b1b453-66e9-4724-a956-26cea2d7d744">EnumSystemLocalesEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2ca39b78-4cbd-4326-95e5-cb233941968f">LOCALE_NEUTRALDATA</a>
</li>
<li>
<a href="https://msdn.microsoft.com/12b8e3dc-20bc-451e-b375-f533b403d159">LOCALE_REPLACEMENT</a>
<div class="alert"><b>Note</b>  This constant is not a valid input to the <i>dwFlags</i> parameter of <a href="https://msdn.microsoft.com/74b1b453-66e9-4724-a956-26cea2d7d744">EnumSystemLocalesEx</a>. To enumerate replacement locales, the application should call this function with the <i>dwFlags</i> parameter specified as LOCALE_WINDOWS or LOCALE_ALL, then check for this constant in the callback function.</div>
<div> </div>
</li>
<li>
<a href="https://msdn.microsoft.com/288026bc-4d73-45a7-809a-0385fc678c8d">LOCALE_SUPPLEMENTAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/931ec33d-d1d0-4a6b-aa55-61db2631dd4f">LOCALE_WINDOWS</a>
</li>
</ul>

#### - lParam [in]

An application-provided input parameter of <a href="https://msdn.microsoft.com/74b1b453-66e9-4724-a956-26cea2d7d744">EnumSystemLocalesEx</a>. This value is especially useful for multi-threaded applications, since it can be used to pass thread-specific data to this callback function.


#### - lpLocaleString [in]

Pointer to a buffer containing a null-terminated <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a> string.


## -returns



Returns <b>TRUE</b> to continue enumeration or <b>FALSE</b> otherwise.




## -remarks



An <b>EnumLocalesProcEx</b> function can carry out any desired task. The application registers this function by passing its address to the <a href="https://msdn.microsoft.com/74b1b453-66e9-4724-a956-26cea2d7d744">EnumSystemLocalesEx</a> function.




## -see-also




<a href="https://msdn.microsoft.com/74b1b453-66e9-4724-a956-26cea2d7d744">EnumSystemLocalesEx</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

