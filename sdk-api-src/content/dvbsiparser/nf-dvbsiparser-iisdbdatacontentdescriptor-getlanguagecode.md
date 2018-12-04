---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetLanguageCode
title: IIsdbDataContentDescriptor::GetLanguageCode
author: windows-sdk-content
description: Gets the three-character ISO 639 language code from an Integrated Services Digital Broadcasting (ISDB) data content descriptor.
old-location: mstv\iisdbdatacontentdescriptor_getlanguagecode.htm
tech.root: mstv
ms.assetid: bbf89870-e258-43d8-8312-edc53998e51a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetLanguageCode, GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetLanguageCode method, IIsdbDataContentDescriptor.GetLanguageCode, IIsdbDataContentDescriptor::GetLanguageCode, dvbsiparser/IIsdbDataContentDescriptor::GetLanguageCode, mstv.iisdbdatacontentdescriptor_getlanguagecode
ms.prod: windows-hardware
ms.technology: windows-devices
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




<a href="https://msdn.microsoft.com/91d55991-5994-4104-9a8f-01cfc347a96f">IIsdbDataContentDescriptor</a>
 

 

