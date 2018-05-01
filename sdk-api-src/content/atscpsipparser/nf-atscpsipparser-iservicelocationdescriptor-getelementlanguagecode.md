---
UID: NF:atscpsipparser.IServiceLocationDescriptor.GetElementLanguageCode
title: IServiceLocationDescriptor::GetElementLanguageCode method
author: windows-driver-content
description: Gets the three-character ISO 639 language code for an Advanced Television Systems Committee (ATSC) service location descriptor.
old-location: mstv\iservicelocationdescriptor_getelementlanguagecode.htm
old-project: mstv
ms.assetid: 8ffc0c58-1305-49bf-bdbd-efb18805516f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetElementLanguageCode method [Microsoft TV Technologies], GetElementLanguageCode method [Microsoft TV Technologies], IServiceLocationDescriptor interface, GetElementLanguageCode,IServiceLocationDescriptor.GetElementLanguageCode, IServiceLocationDescriptor, IServiceLocationDescriptor interface [Microsoft TV Technologies], GetElementLanguageCode method, IServiceLocationDescriptor::GetElementLanguageCode, atscpsipparser/IServiceLocationDescriptor::GetElementLanguageCode, mstv.iservicelocationdescriptor_getelementlanguagecode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: atscpsipparser.h
req.include-header: Atscpsipparser.idl
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IServiceLocationDescriptor.GetElementLanguageCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceLocationDescriptor::GetElementLanguageCode method


## -description


Gets the three-character ISO 639 language code  for an Advanced Television Systems Committee (ATSC) service location descriptor. 


## -parameters




### -param bIndex [in]

Specifies the elementary stream,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/134e4051-6a73-4420-b12d-3171738bd8ad">IServiceLocationDescriptor::GetNumberOfElements</a>
  method to get the number of elementary streams in the descriptor.


### -param LangCode [out]

Pointer to a buffer that receives the language code. For a list of language codes, refer to <a href="http://go.microsoft.com/fwlink?linkID=161422">ISO 639 Code Tables</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/43dd800b-c51d-4a2f-ad59-943cb4975066">IServiceLocationDescriptor</a>
 

 

