---
UID: NF:mfidl.IMFMetadata.SetLanguage
title: IMFMetadata::SetLanguage
author: windows-sdk-content
description: Sets the language for setting and retrieving metadata.
old-location: mf\imfmetadata_setlanguage.htm
tech.root: medfound
ms.assetid: da615053-ddd5-448e-905c-b060cdaefa95
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMFMetadata interface [Media Foundation],SetLanguage method, IMFMetadata.SetLanguage, IMFMetadata::SetLanguage, SetLanguage, SetLanguage method [Media Foundation], SetLanguage method [Media Foundation],IMFMetadata interface, da615053-ddd5-448e-905c-b060cdaefa95, mf.imfmetadata_setlanguage, mfidl/IMFMetadata::SetLanguage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMetadata.SetLanguage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMetadata::SetLanguage


## -description


Sets the language for setting and retrieving metadata.
        


## -parameters




### -param pwszRFC1766 [in]

Pointer to a null-terminated string containing an RFC 1766-compliant language tag.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For more information about language tags, see RFC 1766, "Tags for the Identification of Languages".




## -see-also




<a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a>



<a href="https://msdn.microsoft.com/dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9">Media Metadata</a>
 

 

