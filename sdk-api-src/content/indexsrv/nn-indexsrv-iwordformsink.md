---
UID: NN:indexsrv.IWordFormSink
title: IWordFormSink (indexsrv.h)
author: windows-sdk-content
description: Handles the list of alternative word forms that stemmers generate during query time.
old-location: search\iwordformsink.htm
tech.root: search
ms.assetid: 81D52B0C-BADD-48C0-85DB-57CA82D7BBA8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWordFormSink, IWordFormSink interface [search], IWordFormSink interface [search],described, indexsrv/IWordFormSink, search.iwordformsink
ms.topic: interface
f1_keywords: 
 - "indexsrv/IWordFormSink"
req.header: indexsrv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Indexsrv.h
api_name:
 - IWordFormSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWordFormSink interface


## -description


Handles the list of alternative word forms that stemmers generate during query time.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWordFormSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWordFormSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWordFormSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/search/iwordformsink-putphrase">PutAltWord</a>
</td>
<td align="left" width="63%">
Puts an alternative form of a word in the <b>IWordFormSink</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/search/iwordformsink-putword">PutWord</a>
</td>
<td align="left" width="63%">
Puts the original word form in the <b>IWordFormSink</b> object.

</td>
</tr>
</table> 


## -remarks



Windows Search creates and initializes instances of the StemSink object. The <b>IWordFormSink</b> object receives the <i>ulMaxTokenSize</i> parameter during initialization. The value for this parameter is determined by the <a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nn-indexsrv-istemmer">IStemmer</a> implementation and determines the maximum length, in characters, for a single word that the <b>IWordFormSink</b> handles.




<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nn-indexsrv-istemmer">IStemmer</a> implementations receive a pointer to the <b>IWordFormSink</b> object in the <a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-istemmer-generatewordforms">GenerateWordForms</a> method.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nn-indexsrv-istemmer">IStemmer</a>
 

 

