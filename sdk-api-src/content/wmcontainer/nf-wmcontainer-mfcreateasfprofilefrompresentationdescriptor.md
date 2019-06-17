---
UID: NF:wmcontainer.MFCreateASFProfileFromPresentationDescriptor
title: MFCreateASFProfileFromPresentationDescriptor function (wmcontainer.h)
author: windows-sdk-content
description: Creates an ASF profile object from a presentation descriptor.
old-location: mf\mfcreateasfprofilefrompresentationdescriptor.htm
tech.root: medfound
ms.assetid: 1163d958-fbea-48f3-9ac3-1595c0cc2d32
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 1163d958-fbea-48f3-9ac3-1595c0cc2d32, MFCreateASFProfileFromPresentationDescriptor, MFCreateASFProfileFromPresentationDescriptor function [Media Foundation], mf.mfcreateasfprofilefrompresentationdescriptor, wmcontainer/MFCreateASFProfileFromPresentationDescriptor
ms.topic: function
f1_keywords: ["wmcontainer/MFCreateASFProfileFromPresentationDescriptor"]
req.header: wmcontainer.h
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
 - MFCreateASFProfileFromPresentationDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateASFProfileFromPresentationDescriptor function


## -description



Creates an ASF profile object from a presentation descriptor.




## -parameters




### -param pIPD

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface of the presentation descriptor that contains the profile information.


### -param ppIProfile

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a> interface. The caller must release the interface.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

