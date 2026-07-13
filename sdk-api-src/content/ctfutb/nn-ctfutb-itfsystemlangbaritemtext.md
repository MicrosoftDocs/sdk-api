---
UID: NN:ctfutb.ITfSystemLangBarItemText
title: ITfSystemLangBarItemText (ctfutb.h)
description: The ITfSystemLangBarItemText interface is implemented by a system language bar and is used by a system language bar extension to modify the description displayed for the menu.
helpviewer_keywords: ["ITfSystemLangBarItemText","ITfSystemLangBarItemText interface [Text Services Framework]","ITfSystemLangBarItemText interface [Text Services Framework]","described","_tsf_itfsystemlangbaritemtext_ref","ctfutb/ITfSystemLangBarItemText","tsf.itfsystemlangbaritemtext"]
old-location: tsf\itfsystemlangbaritemtext.htm
tech.root: TSF
ms.assetid: f39ec024-1bdf-4451-9598-1953bffc9704
ms.date: 12/05/2018
ms.keywords: ITfSystemLangBarItemText, ITfSystemLangBarItemText interface [Text Services Framework], ITfSystemLangBarItemText interface [Text Services Framework],described, _tsf_itfsystemlangbaritemtext_ref, ctfutb/ITfSystemLangBarItemText, tsf.itfsystemlangbaritemtext
req.header: ctfutb.h
req.include-header: Msctf.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfSystemLangBarItemText
 - ctfutb/ITfSystemLangBarItemText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ctfutb.h
api_name:
 - ITfSystemLangBarItemText
---

# ITfSystemLangBarItemText interface


## -description

The <b>ITfSystemLangBarItemText</b> interface is implemented by a system language bar and is used by a system language bar extension to modify the description displayed for the menu. The extension can obtain an instance of this interface by calling the menu object QueryInterface method with IID_ITfSystemLangBarItem.

## -inheritance

The <b>ITfSystemLangBarItemText</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfSystemLangBarItemText</b> also has these types of members:

