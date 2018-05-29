---
UID: NF:dvbsiparser.IDvbShortEventDescriptor.GetLanguageCode
title: IDvbShortEventDescriptor::GetLanguageCode
author: windows-sdk-content
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) short event descriptor.
old-location: mstv\idvbshorteventdescriptor_getlanguagecode.htm
old-project: mstv
ms.assetid: c531ae74-586f-4191-9b77-5f5837e551c4
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetLanguageCode, GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies],IDvbShortEventDescriptor interface, IDvbShortEventDescriptor interface [Microsoft TV Technologies],GetLanguageCode method, IDvbShortEventDescriptor.GetLanguageCode, IDvbShortEventDescriptor::GetLanguageCode, dvbsiparser/IDvbShortEventDescriptor::GetLanguageCode, mstv.idvbshorteventdescriptor_getlanguagecode
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbShortEventDescriptor.GetLanguageCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbShortEventDescriptor::GetLanguageCode


## -description


Gets the three-character ISO 639 language code from
a Digital Video Broadcast (DVB) short event descriptor.


## -parameters




### -param pszCode

Receives the language code. For a list of language codes, refer to <a href="http://www.sil.org/ISO639-3/codes.asp">this document</a>. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/039ae2e1-1dad-4a70-a054-bd95b0b500fb">IDvbShortEventDescriptor</a>
 

 

