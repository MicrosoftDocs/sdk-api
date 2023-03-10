---
UID: NN:ctfutb.ITfLangBarItemBitmap
title: ITfLangBarItemBitmap (ctfutb.h)
description: The ITfLangBarItemBitmap interface is implemented by an application or text service and used by the language bar manager to obtain information specific to a bitmap item on the language bar.
helpviewer_keywords: ["ITfLangBarItemBitmap","ITfLangBarItemBitmap interface [Text Services Framework]","ITfLangBarItemBitmap interface [Text Services Framework]","described","_tsf_itflangbaritembitmap_ref","ctfutb/ITfLangBarItemBitmap","tsf.itflangbaritembitmap"]
old-location: tsf\itflangbaritembitmap.htm
tech.root: TSF
ms.assetid: 3bae0422-625e-4f7d-9845-5353ad3ff335
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemBitmap, ITfLangBarItemBitmap interface [Text Services Framework], ITfLangBarItemBitmap interface [Text Services Framework],described, _tsf_itflangbaritembitmap_ref, ctfutb/ITfLangBarItemBitmap, tsf.itflangbaritembitmap
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
 - ITfLangBarItemBitmap
 - ctfutb/ITfLangBarItemBitmap
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
 - ITfLangBarItemBitmap
---

# ITfLangBarItemBitmap interface


## -description

The <b>ITfLangBarItemBitmap</b> interface is implemented by an application or text service and used by the language bar manager to obtain information specific to a bitmap item on the language bar.

The language bar manager obtains an instance of this interface by calling QueryInterface on the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> passed to <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem</a> with IID_ITfLangBarItemBitmap.

## -inheritance

The <b>ITfLangBarItemBitmap</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarItemBitmap</b> also has these types of members:

## -remarks

A language bar bitmap functions as a static item on the language bar that displays a bitmap.

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem
      </a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
