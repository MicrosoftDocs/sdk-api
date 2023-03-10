---
UID: NF:wdsclientapi.WdsCliGetImageArchitecture
title: WdsCliGetImageArchitecture function (wdsclientapi.h)
description: Returns the processor architecture for the current image.
helpviewer_keywords: ["PROCESSOR_ARCHITECTURE_AMD64","PROCESSOR_ARCHITECTURE_IA64","PROCESSOR_ARCHITECTURE_INTEL","WdsCliGetImageArchitecture","WdsCliGetImageArchitecture function [Windows Deployment Services]","wds.wdscligetimagearchitecture","wdsclientapi/WdsCliGetImageArchitecture"]
old-location: wds\wdscligetimagearchitecture.htm
tech.root: wds
ms.assetid: 69df2926-e0f1-4c52-bc91-7d2e1391f835
ms.date: 12/05/2018
ms.keywords: PROCESSOR_ARCHITECTURE_AMD64, PROCESSOR_ARCHITECTURE_IA64, PROCESSOR_ARCHITECTURE_INTEL, WdsCliGetImageArchitecture, WdsCliGetImageArchitecture function [Windows Deployment Services], wds.wdscligetimagearchitecture, wdsclientapi/WdsCliGetImageArchitecture
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsCliGetImageArchitecture
 - wdsclientapi/WdsCliGetImageArchitecture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliGetImageArchitecture
---

# WdsCliGetImageArchitecture function


## -description

Returns the processor architecture for the current image.

## -parameters

### -param hIfh [in]

A find handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.

### -param pdwValue [out]

Pointer to a value that describes the processor architecture of the current image. 
      


This parameter can have one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_AMD64"></a><a id="processor_architecture_amd64"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_AMD64</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The image is an x64 image (AMD AMD64 or Intel EM64T).

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_IA64"></a><a id="processor_architecture_ia64"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_IA64</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The image is an Itanium-based system image.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_INTEL"></a><a id="processor_architecture_intel"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_INTEL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The image is a 32-bit Intel x86 image.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This value 
      is valid until the 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> or 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a> function is used to change or close the 
      current handle.

## -see-also

<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a>



<a href="/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>