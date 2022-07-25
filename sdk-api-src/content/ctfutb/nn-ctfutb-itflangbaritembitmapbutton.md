---
UID: NN:ctfutb.ITfLangBarItemBitmapButton
title: ITfLangBarItemBitmapButton (ctfutb.h)
description: The ITfLangBarItemBitmapButton interface is implemented by a language bar bitmap button provider and is used by the language bar manager to obtain information specific to a bitmap button item on the language bar.
helpviewer_keywords: ["ITfLangBarItemBitmapButton","ITfLangBarItemBitmapButton interface [Text Services Framework]","ITfLangBarItemBitmapButton interface [Text Services Framework]","described","_tsf_itflangbaritembitmapbutton_ref","ctfutb/ITfLangBarItemBitmapButton","tsf.itflangbaritembitmapbutton"]
old-location: tsf\itflangbaritembitmapbutton.htm
tech.root: TSF
ms.assetid: 29fcc913-fcc7-4321-918b-2c354dd751ff
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemBitmapButton, ITfLangBarItemBitmapButton interface [Text Services Framework], ITfLangBarItemBitmapButton interface [Text Services Framework],described, _tsf_itflangbaritembitmapbutton_ref, ctfutb/ITfLangBarItemBitmapButton, tsf.itflangbaritembitmapbutton
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
 - ITfLangBarItemBitmapButton
 - ctfutb/ITfLangBarItemBitmapButton
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
 - ITfLangBarItemBitmapButton
---

# ITfLangBarItemBitmapButton interface


## -description

The <b>ITfLangBarItemBitmapButton</b> interface is implemented by a language bar bitmap button provider and is used by the language bar manager to obtain information specific to a bitmap button item on the language bar.

The language bar manager obtains an instance of this interface by calling QueryInterface on the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> passed to <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem</a> with IID_ITfLangBarItemBitmapButton.

## -inheritance

The <b>ITfLangBarItemBitmapButton</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarItemBitmapButton</b> also has these types of members:

## -remarks

A language bar bitmap button functions as a button item on the language bar that displays text and a small bitmap. The bitmap displayed for the item should not be larger than the size of a small icon. Obtain these dimensions by calling <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with SM_CXSMICON for the width and SM_CYSMICON for the height.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem
      </a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
