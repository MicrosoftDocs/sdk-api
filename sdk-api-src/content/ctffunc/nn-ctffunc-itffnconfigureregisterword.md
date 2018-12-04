---
UID: NN:ctffunc.ITfFnConfigureRegisterWord
title: ITfFnConfigureRegisterWord
author: windows-sdk-content
description: The ITfFnConfigureRegisterWord interface is implemented by a text service to enable the Active Input Method Editor (IME) to cause the text service to display a word registration dialog box.
old-location: tsf\itffnconfigureregisterword.htm
tech.root: TSF
ms.assetid: 515e5f01-a68f-4e67-acf5-cac1923d485e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITfFnConfigureRegisterWord, ITfFnConfigureRegisterWord interface [Text Services Framework], ITfFnConfigureRegisterWord interface [Text Services Framework],described, _tsf_itffnconfigureregisterword_ref, ctffunc/ITfFnConfigureRegisterWord, tsf.itffnconfigureregisterword
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfFnConfigureRegisterWord
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnConfigureRegisterWord interface


## -description


The <b>ITfFnConfigureRegisterWord</b> interface is implemented by a text service to enable the Active Input Method Editor (IME) to cause the text service to display a word registration dialog box.

To obtain an instance of this interface the IME can call <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> with IID_ITfFnConfigureRegisterWord.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnConfigureRegisterWord</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnConfigureRegisterWord</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnConfigureRegisterWord</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61eb7452-2ada-4832-bd16-87ac56fedc6d">Show</a>
</td>
<td align="left" width="63%">
Called to cause the text service to display a dialog box to register a word with the text service.

</td>
</tr>
</table> 

