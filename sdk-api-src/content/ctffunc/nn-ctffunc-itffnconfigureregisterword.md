---
UID: NN:ctffunc.ITfFnConfigureRegisterWord
title: ITfFnConfigureRegisterWord (ctffunc.h)
description: The ITfFnConfigureRegisterWord interface is implemented by a text service to enable the Active Input Method Editor (IME) to cause the text service to display a word registration dialog box.
helpviewer_keywords: ["ITfFnConfigureRegisterWord","ITfFnConfigureRegisterWord interface [Text Services Framework]","ITfFnConfigureRegisterWord interface [Text Services Framework]","described","_tsf_itffnconfigureregisterword_ref","ctffunc/ITfFnConfigureRegisterWord","tsf.itffnconfigureregisterword"]
old-location: tsf\itffnconfigureregisterword.htm
tech.root: TSF
ms.assetid: 515e5f01-a68f-4e67-acf5-cac1923d485e
ms.date: 12/05/2018
ms.keywords: ITfFnConfigureRegisterWord, ITfFnConfigureRegisterWord interface [Text Services Framework], ITfFnConfigureRegisterWord interface [Text Services Framework],described, _tsf_itffnconfigureregisterword_ref, ctffunc/ITfFnConfigureRegisterWord, tsf.itffnconfigureregisterword
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfFnConfigureRegisterWord
 - ctffunc/ITfFnConfigureRegisterWord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfFnConfigureRegisterWord
---

# ITfFnConfigureRegisterWord interface


## -description

The <b>ITfFnConfigureRegisterWord</b> interface is implemented by a text service to enable the Active Input Method Editor (IME) to cause the text service to display a word registration dialog box.

To obtain an instance of this interface the IME can call <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> with IID_ITfFnConfigureRegisterWord.

## -inheritance

The <b>ITfFnConfigureRegisterWord</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnConfigureRegisterWord</b> also has these types of members:

