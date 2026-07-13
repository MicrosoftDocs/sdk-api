---
UID: NN:ctfutb.ITfLangBarItemBalloon
title: ITfLangBarItemBalloon (ctfutb.h)
description: The ITfLangBarItemBalloon interface is implemented by an application or text service and is used by the language bar manager to obtain information specific to a balloon item on the language bar.
helpviewer_keywords: ["ITfLangBarItemBalloon","ITfLangBarItemBalloon interface [Text Services Framework]","ITfLangBarItemBalloon interface [Text Services Framework]","described","_tsf_itflangbaritemballoon_ref","ctfutb/ITfLangBarItemBalloon","tsf.itflangbaritemballoon"]
old-location: tsf\itflangbaritemballoon.htm
tech.root: TSF
ms.assetid: 619a6f21-fbac-455c-a702-0302ce13112b
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemBalloon, ITfLangBarItemBalloon interface [Text Services Framework], ITfLangBarItemBalloon interface [Text Services Framework],described, _tsf_itflangbaritemballoon_ref, ctfutb/ITfLangBarItemBalloon, tsf.itflangbaritemballoon
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
 - ITfLangBarItemBalloon
 - ctfutb/ITfLangBarItemBalloon
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
 - ITfLangBarItemBalloon
---

# ITfLangBarItemBalloon interface


## -description

The <b>ITfLangBarItemBalloon</b> interface is implemented by an application or text service and is used by the language bar manager to obtain information specific to a balloon item on the language bar.

The language bar manager obtains an instance of this interface by calling QueryInterface on the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> passed to <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem</a> with IID_ITfLangBarItemBalloon.

## -inheritance

The <b>ITfLangBarItemBalloon</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarItemBalloon</b> also has these types of members:

## -remarks

A language bar balloon acts as a pop-up notification on the language bar.

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem
      </a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
