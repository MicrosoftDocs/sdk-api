---
UID: NF:wmcontainer.IMFASFContentInfo.GeneratePresentationDescriptor
title: IMFASFContentInfo::GeneratePresentationDescriptor (wmcontainer.h)
description: Creates a presentation descriptor for ASF content.
helpviewer_keywords: ["GeneratePresentationDescriptor","GeneratePresentationDescriptor method [Media Foundation]","GeneratePresentationDescriptor method [Media Foundation]","IMFASFContentInfo interface","IMFASFContentInfo interface [Media Foundation]","GeneratePresentationDescriptor method","IMFASFContentInfo.GeneratePresentationDescriptor","IMFASFContentInfo::GeneratePresentationDescriptor","f22cb48d-1346-4182-8ca2-f57a7fdc76e4","mf.imfasfcontentinfo_generatepresentationdescriptor","wmcontainer/IMFASFContentInfo::GeneratePresentationDescriptor"]
old-location: mf\imfasfcontentinfo_generatepresentationdescriptor.htm
tech.root: mf
ms.assetid: f22cb48d-1346-4182-8ca2-f57a7fdc76e4
ms.date: 12/05/2018
ms.keywords: GeneratePresentationDescriptor, GeneratePresentationDescriptor method [Media Foundation], GeneratePresentationDescriptor method [Media Foundation],IMFASFContentInfo interface, IMFASFContentInfo interface [Media Foundation],GeneratePresentationDescriptor method, IMFASFContentInfo.GeneratePresentationDescriptor, IMFASFContentInfo::GeneratePresentationDescriptor, f22cb48d-1346-4182-8ca2-f57a7fdc76e4, mf.imfasfcontentinfo_generatepresentationdescriptor, wmcontainer/IMFASFContentInfo::GeneratePresentationDescriptor
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFContentInfo::GeneratePresentationDescriptor
 - wmcontainer/IMFASFContentInfo::GeneratePresentationDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFContentInfo.GeneratePresentationDescriptor
---

# IMFASFContentInfo::GeneratePresentationDescriptor


## -description

Creates a presentation descriptor for ASF content.

## -parameters

### -param ppIPresentationDescriptor [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/asf-contentinfo-object">ASF ContentInfo Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a>