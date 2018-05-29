---
UID: NF:wmcontainer.IMFASFContentInfo.GeneratePresentationDescriptor
title: IMFASFContentInfo::GeneratePresentationDescriptor
author: windows-sdk-content
description: Creates a presentation descriptor for ASF content.
old-location: mf\imfasfcontentinfo_generatepresentationdescriptor.htm
old-project: medfound
ms.assetid: f22cb48d-1346-4182-8ca2-f57a7fdc76e4
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GeneratePresentationDescriptor, GeneratePresentationDescriptor method [Media Foundation], GeneratePresentationDescriptor method [Media Foundation],IMFASFContentInfo interface, IMFASFContentInfo interface [Media Foundation],GeneratePresentationDescriptor method, IMFASFContentInfo.GeneratePresentationDescriptor, IMFASFContentInfo::GeneratePresentationDescriptor, f22cb48d-1346-4182-8ca2-f57a7fdc76e4, mf.imfasfcontentinfo_generatepresentationdescriptor, wmcontainer/IMFASFContentInfo::GeneratePresentationDescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFASFContentInfo.GeneratePresentationDescriptor
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFContentInfo::GeneratePresentationDescriptor


## -description



Creates a presentation descriptor for ASF content.




## -parameters




### -param ppIPresentationDescriptor [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ASF ContentInfo Object</a>



<a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a>
 

 

