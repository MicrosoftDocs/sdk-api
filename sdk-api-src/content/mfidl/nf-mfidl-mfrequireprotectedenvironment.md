---
UID: NF:mfidl.MFRequireProtectedEnvironment
title: MFRequireProtectedEnvironment function
author: windows-sdk-content
description: Queries whether a media presentation requires the Protected Media Path (PMP).
old-location: mf\mfrequireprotectedenvironment.htm
tech.root: medfound
ms.assetid: 5129d8c0-4049-4b90-ade8-b4cd32277664
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5129d8c0-4049-4b90-ade8-b4cd32277664, MFRequireProtectedEnvironment, MFRequireProtectedEnvironment function [Media Foundation], mf.mfrequireprotectedenvironment, mfidl/MFRequireProtectedEnvironment
ms.topic: function
req.header: mfidl.h
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFRequireProtectedEnvironment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFRequireProtectedEnvironment function


## -description



Queries whether a media presentation requires the Protected Media Path (PMP).




## -parameters




### -param pPresentationDescriptor [in]

Pointer to the <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface of a presentation descriptor. The presentation descriptor is created by the media source, and describes the presentation.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
This presentation requires a protected environment.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
This presentation does not require a protected environment.

</td>
</tr>
</table>
 




## -remarks



If this function returns <b>S_OK</b>, it means the PMP is required for this presentation. Call <a href="https://msdn.microsoft.com/cb492e68-3d8a-49b2-8c0b-bee8065b53a8">MFCreatePMPMediaSession</a> to create the PMP session object.

If the function returns <b>S_FALSE</b>, you can use the unprotected pipeline. Call <a href="https://msdn.microsoft.com/86b2b5ec-231c-4943-9add-1a5a60e72268">MFCreateMediaSession</a> to create the regular Media Session object.

Internally, this function checks whether any of the stream descriptors in the presentation have the <a href="https://msdn.microsoft.com/1c1a201c-4b55-4b86-a08f-d06c1a7db29d">MF_SD_PROTECTED</a> attribute with the value <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

