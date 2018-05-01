---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetLanguageCode
title: IDvbComponentDescriptor::GetLanguageCode method
author: windows-driver-content
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) component descriptor.
old-location: mstv\idvbcomponentdescriptor_getlanguagecode.htm
old-project: mstv
ms.assetid: 9898cd33-db5d-41d3-9e3d-77da2ff38e44
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies], IDvbComponentDescriptor interface, GetLanguageCode,IDvbComponentDescriptor.GetLanguageCode, IDvbComponentDescriptor, IDvbComponentDescriptor interface [Microsoft TV Technologies], GetLanguageCode method, IDvbComponentDescriptor::GetLanguageCode, dvbsiparser/IDvbComponentDescriptor::GetLanguageCode, mstv.idvbcomponentdescriptor_getlanguagecode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbComponentDescriptor.GetLanguageCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbComponentDescriptor::GetLanguageCode method


## -description


Gets the three-character ISO 639 language code from
a Digital Video Broadcast (DVB) component descriptor.


## -parameters




### -param pszCode

Pointer to the buffer that receives the language code. For a list of language codes, refer to the <a href="http://www.sil.org/ISO639-3/codes.asp">ISO 639 Code Tables</a>. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0dee15ee-5b36-4454-8092-6b57ef5063ce">IDvbComponentDescriptor</a>
 

 

