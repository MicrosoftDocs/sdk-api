---
UID: NN:ctfutb.ITfLangBarItemMgr
title: ITfLangBarItemMgr (ctfutb.h)
description: The ITfLangBarItemMgr interface is implemented by the language bar and used by a text service to manage items in the language bar.
helpviewer_keywords: ["ITfLangBarItemMgr","ITfLangBarItemMgr interface [Text Services Framework]","ITfLangBarItemMgr interface [Text Services Framework]","described","_tsf_itflangbaritemmgr_ref","ctfutb/ITfLangBarItemMgr","tsf.itflangbaritemmgr"]
old-location: tsf\itflangbaritemmgr.htm
tech.root: TSF
ms.assetid: a7fa257f-e600-4554-8b23-f73323f37e69
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemMgr, ITfLangBarItemMgr interface [Text Services Framework], ITfLangBarItemMgr interface [Text Services Framework],described, _tsf_itflangbaritemmgr_ref, ctfutb/ITfLangBarItemMgr, tsf.itflangbaritemmgr
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfLangBarItemMgr
 - ctfutb/ITfLangBarItemMgr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLangBarItemMgr
---

# ITfLangBarItemMgr interface


## -description

The <b>ITfLangBarItemMgr</b> interface is implemented by the language bar and used by a text service to manage items in the language bar.

A text service obtains an instance of this interface by calling ITfThreadMgr::QueryInterface with IID_ITfLangBarItemMgr. An instance of this interface can also be created by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with CLSID_TF_LangBarItemMgr.

## -inheritance

The <b>ITfLangBarItemMgr</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarItemMgr</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
