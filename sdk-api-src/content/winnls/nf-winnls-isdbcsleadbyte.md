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

# IsDBCSLeadByte function


## -description


Determines if a specified character is a lead byte for the system default Windows ANSI code page 
    (<b>CP_ACP</b>). A lead byte is the first byte of a two-byte character in a 
    <a href="https://msdn.microsoft.com/df049d22-02e2-48b2-8b74-52f71c00c549">double-byte character set</a> (DBCS) for the code 
    page.
<div class="alert"><b>Note</b>  To use a different code page, your application should use the 
    <a href="https://msdn.microsoft.com/1ca67e7e-a2a7-433f-b2b6-8fa5ecc50354">IsDBCSLeadByteEx</a> function.</div><div> </div>

## -parameters




### -param TestChar [in]

The character to test.


## -returns



Returns a nonzero value if the test character is potentially a lead byte. The function returns 0 if the test 
       character is not a lead byte or if it is a single-byte character. To get extended error information, the 
       application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  This function does not validate the presence or validity of a trail byte. Therefore, 
     <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> might not recognize a 
     sequence that the application using <b>IsDBCSLeadByte</b> 
     reports as a lead byte. The application can easily become unsynchronized with the results of 
     <b>MultiByteToWideChar</b>, potentially leading to 
     unexpected errors or buffer size mismatches.</div>
<div> </div>
In general, instead of attempting low-level manipulation of code page data, applications should use 
    <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> to convert the 
    data to UTF-16 and work with it in that encoding.

Lead byte values are specific to each distinct DBCS. Some byte values can appear in a single code page as both 
    the lead and trail byte of a DBCS character.

To make sense of a DBCS string, an application normally starts at the beginning of a string and scans forward, 
    keeping track when it encounters a lead byte, and treating the next byte as the trailing part of the same 
    character. If the application must back up, it should use 
    <a href="_win32_CharPrev_cpp">CharPrev</a> instead of attempting to develop its own 
    algorithm.




## -see-also




<a href="https://msdn.microsoft.com/1ca67e7e-a2a7-433f-b2b6-8fa5ecc50354">IsDBCSLeadByteEx</a>



<a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a>



<a href="https://msdn.microsoft.com/1799f5da-1391-4b6e-ac13-718017a77557">Unicode and Character Set Functions</a>



<a href="https://msdn.microsoft.com/8c1c6582-b58c-4008-9ce5-208acc191d9f">Unicode and Character Sets</a>
 

 

