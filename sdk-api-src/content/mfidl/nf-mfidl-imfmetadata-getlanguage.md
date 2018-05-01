---
UID: NF:mfidl.IMFMetadata.GetLanguage
title: IMFMetadata::GetLanguage method
author: windows-driver-content
description: Gets the current language setting.
old-location: mf\imfmetadata_getlanguage.htm
old-project: medfound
ms.assetid: 75295c93-a389-42c4-aa56-debc36a5f532
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 75295c93-a389-42c4-aa56-debc36a5f532, GetLanguage method [Media Foundation], GetLanguage method [Media Foundation], IMFMetadata interface, GetLanguage,IMFMetadata.GetLanguage, IMFMetadata, IMFMetadata interface [Media Foundation], GetLanguage method, IMFMetadata::GetLanguage, mf.imfmetadata_getlanguage, mfidl/IMFMetadata::GetLanguage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMetadata.GetLanguage
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMetadata::GetLanguage method


## -description



          Gets the current language setting.


## -parameters




### -param ppwszRFC1766 [out]


            Receives a pointer to a null-terminated string containing an RFC 1766-compliant language tag. The caller must release the string by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.
          


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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The metadata provider does not support multiple languages.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">

                No language was set.
              

</td>
</tr>
</table>
 




## -remarks



For more information about language tags, see RFC 1766, "Tags for the Identification of Languages."

The <a href="https://msdn.microsoft.com/da615053-ddd5-448e-905c-b060cdaefa95">IMFMetadata::SetLanguage</a> and <a href="https://msdn.microsoft.com/177c8612-5c9f-4a71-9ee1-a4c67737af2d">IMFMetadata::GetProperty</a> methods set and get metadata for the current language setting.




## -see-also




<a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a>



<a href="https://msdn.microsoft.com/dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9">Media Metadata</a>
 

 

