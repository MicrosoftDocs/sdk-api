---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPhraseSink::PutSmallPhrase


## -description


Puts a small query-time phrase in the <a href="https://msdn.microsoft.com/9485202D-94D6-4E9E-9C42-502033E85670">IPhraseSink</a> object for WordBreaker.


## -parameters




### -param pwcNoun [in]

A pointer to a buffer that contains a word being modified.


### -param cwcNoun [in]

The number of characters in <i>pwcNoun</i>. There is no limit on the size of a query-time phrase.


### -param pwcModifier [in]

A pointer to the word modifying <i>pwcNoun</i>.


### -param cwcModifier [in]

The number of characters in <i>pwcModifier</i>. There is no limit on the size of a query-time phrase.


### -param ulAttachmentType [in]

A wordbreaker-specific value which a 
 wordbreaker can use to store additional information about the method of composition.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



<b>PutSmallPhrase</b> is called by the <a href="https://msdn.microsoft.com/32e495c0-e173-4b35-be58-51f31cb38e3e">IWordBreaker::BreakText</a> method of the <a href="https://msdn.microsoft.com/36c46931-5c5c-4ab9-9291-60ad93cebbf0">IWordBreaker</a> implementation. Phrases that the <a href="https://msdn.microsoft.com/9485202D-94D6-4E9E-9C42-502033E85670">IPhraseSink</a> object handles are used by Windows Search to expand the original query text.






## -see-also




<a href="https://msdn.microsoft.com/9485202D-94D6-4E9E-9C42-502033E85670">IPhraseSink</a>
 

 

