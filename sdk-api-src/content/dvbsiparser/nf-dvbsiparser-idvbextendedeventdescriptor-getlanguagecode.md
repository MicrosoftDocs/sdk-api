---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetLanguageCode
title: IDvbExtendedEventDescriptor::GetLanguageCode
author: windows-sdk-content
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) extended event descriptor.
old-location: mstv\idvbextendedeventdescriptor_getlanguagecode.htm
old-project: mstv
ms.assetid: f63b7fa9-969e-43d4-95f3-445d6265f445
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetLanguageCode, GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetLanguageCode method, IDvbExtendedEventDescriptor.GetLanguageCode, IDvbExtendedEventDescriptor::GetLanguageCode, dvbsiparser/IDvbExtendedEventDescriptor::GetLanguageCode, mstv.idvbextendedeventdescriptor_getlanguagecode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbExtendedEventDescriptor.GetLanguageCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbExtendedEventDescriptor::GetLanguageCode


## -description


Gets the three-character ISO 639 language code from
a Digital Video Broadcast (DVB) extended event descriptor.


## -parameters




### -param pszCode

Pointer to the buffer that receives the language code. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/db100f17-f7b8-4252-8090-44567ab9dcbe">IDvbExtendedEventDescriptor</a>
 

 

