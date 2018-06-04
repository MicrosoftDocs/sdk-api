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

# CheckColorsInGamut function


## -description


The <b>CheckColorsInGamut</b> function determines whether a specified set of RGB triples lies in the output <a href="g.htm">gamut</a> of a specified device. The RGB triples are interpreted in the input logical color space.


## -parameters




### -param hdc

TBD


### -param lpRGBTriple

TBD


### -param dlpBuffer

TBD


### -param nCount

The number of elements in the array of triples.


#### - hDC

Handle to the device context whose output gamut to be checked.


#### - lpBuffer

Pointer to the buffer in which the results are to be placed. This buffer must be at least as large as <i>nCount</i> bytes.


#### - lpRGBTriples

Pointer to an array of RGB triples to check.


## -returns



If this function succeeds, the return value is a nonzero value.

If this function fails, the return value is zero.




## -remarks



The function places the test results in the buffer pointed to by <i>lpBuffer</i>. Each byte in the buffer corresponds to an <i>RGB triple</i>, and has an unsigned value between CM_IN_GAMUT (= 0) and CM_OUT_OF_GAMUT (= 255). The value 0 denotes that the color is in gamut, while a nonzero value denotes that it is out of gamut. For any integer <i>n</i> such that 0 &lt; <i>n</i> &lt; 255, a result value of <i>n</i> + 1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of <i>n</i>, as specified by the ICC Profile Format Specification. For more information on the ICC Profile Format Specification, see the sources listed in <a href="https://msdn.microsoft.com/6e2ac851-3dba-4bbb-b766-82800b1cc5f1">Further Information</a>.

Note that for this function to succeed, WCS must be enabled for the device context handle that is passed in through the <i>hDC</i> parameter. WCS can be enabled for a device context handle by calling the <a href="https://msdn.microsoft.com/40d70c1f-c580-43c4-b44b-6c9388e138fb">SetICMMode</a> function.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/40d70c1f-c580-43c4-b44b-6c9388e138fb">SetICMMode</a>
 

 

