---
UID: NN:ctfutb.ITfSystemDeviceTypeLangBarItem
title: ITfSystemDeviceTypeLangBarItem (ctfutb.h)
description: The ITfSystemDeviceTypeLangBarItem interface is implemented by a system language bar item and used by an application or text service to control how the system item displays its icon.
helpviewer_keywords: ["ITfSystemDeviceTypeLangBarItem","ITfSystemDeviceTypeLangBarItem interface [Text Services Framework]","ITfSystemDeviceTypeLangBarItem interface [Text Services Framework]","described","_tsf_itfsystemdevicetypelangbaritem_ref","ctfutb/ITfSystemDeviceTypeLangBarItem","tsf.itfsystemdevicetypelangbaritem"]
old-location: tsf\itfsystemdevicetypelangbaritem.htm
tech.root: TSF
ms.assetid: 0dc32f10-eecd-4203-992c-80eb0f991615
ms.date: 12/05/2018
ms.keywords: ITfSystemDeviceTypeLangBarItem, ITfSystemDeviceTypeLangBarItem interface [Text Services Framework], ITfSystemDeviceTypeLangBarItem interface [Text Services Framework],described, _tsf_itfsystemdevicetypelangbaritem_ref, ctfutb/ITfSystemDeviceTypeLangBarItem, tsf.itfsystemdevicetypelangbaritem
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
 - ITfSystemDeviceTypeLangBarItem
 - ctfutb/ITfSystemDeviceTypeLangBarItem
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
 - ITfSystemDeviceTypeLangBarItem
---

# ITfSystemDeviceTypeLangBarItem interface


## -description

The <b>ITfSystemDeviceTypeLangBarItem</b> interface is implemented by a system language bar item and used by an application or text service to control how the system item displays its icon. The application or text service obtains an instance of this interface by calling QueryInterface on the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> object with IID_ITfSystemDeviceTypeLangBarItem.

## -inheritance

The <b>ITfSystemDeviceTypeLangBarItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfSystemDeviceTypeLangBarItem</b> also has these types of members:

## -remarks

Support for this interface is optional and must not be assumed.

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
