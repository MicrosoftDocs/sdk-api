---
UID: NF:indexsrv.IPhraseSink.PutSmallPhrase
title: IPhraseSink::PutSmallPhrase
author: windows-sdk-content
description: Puts a small query-time phrase in the IPhraseSink object for WordBreaker.
old-location: search\iphrasesink_putsmallphrase.htm
tech.root: search
ms.assetid: AC666D12-220B-4D22-997E-CCBE9967B6AB
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IPhraseSink interface [search],PutSmallPhrase method, IPhraseSink.PutSmallPhrase, IPhraseSink::PutSmallPhrase, PutSmallPhrase, PutSmallPhrase method [search], PutSmallPhrase method [search],IPhraseSink interface, indexsrv/IPhraseSink::PutSmallPhrase, search.iphrasesink_putsmallphrase
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: indexsrv.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - indexsrv.h
api_name:
 - IPhraseSink.PutSmallPhrase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

