---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetLanguageCode
title: IIsdbDataContentDescriptor::GetLanguageCode (dvbsiparser.h)
author: windows-sdk-content
description: Gets the three-character ISO 639 language code from an Integrated Services Digital Broadcasting (ISDB) data content descriptor.
old-location: mstv\iisdbdatacontentdescriptor_getlanguagecode.htm
tech.root: mstv
ms.assetid: bbf89870-e258-43d8-8312-edc53998e51a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLanguageCode, GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetLanguageCode method, IIsdbDataContentDescriptor.GetLanguageCode, IIsdbDataContentDescriptor::GetLanguageCode, dvbsiparser/IIsdbDataContentDescriptor::GetLanguageCode, mstv.iisdbdatacontentdescriptor_getlanguagecode
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IIsdbDataContentDescriptor.GetLanguageCode"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbDataContentDescriptor.GetLanguageCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDataContentDescriptor::GetLanguageCode


## -description


 Gets the three-character ISO 639 language code from an Integrated Services Digital Broadcasting (ISDB) data content descriptor.


## -parameters




### -param pszCode

Pointer to the buffer that receives the language code. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>
 

 

