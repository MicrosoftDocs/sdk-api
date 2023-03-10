---
UID: NN:msctf.ITfCategoryMgr
title: ITfCategoryMgr (msctf.h)
description: The ITfCategoryMgr interface manages categories of objects for text services. The TSF manager implements this interface.
helpviewer_keywords: ["ITfCategoryMgr","ITfCategoryMgr interface [Text Services Framework]","ITfCategoryMgr interface [Text Services Framework]","described","_tsf_itfcategorymgr_ref","msctf/ITfCategoryMgr","tsf.itfcategorymgr"]
old-location: tsf\itfcategorymgr.htm
tech.root: TSF
ms.assetid: 26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4
ms.date: 12/05/2018
ms.keywords: ITfCategoryMgr, ITfCategoryMgr interface [Text Services Framework], ITfCategoryMgr interface [Text Services Framework],described, _tsf_itfcategorymgr_ref, msctf/ITfCategoryMgr, tsf.itfcategorymgr
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCategoryMgr
 - msctf/ITfCategoryMgr
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
 - ITfCategoryMgr
---

# ITfCategoryMgr interface


## -description

The <b>ITfCategoryMgr</b> interface manages categories of objects for text services. The TSF manager implements this interface.

TSF categories help organize objects identified by a globally unique identifier ( GUID ). For example, a class identifier ( CLSID ) identifies a text service, and a GUID identifies the TSF compartment, TSF properties, and TSF display attributes. To group and organize multiple GUIDs, TSF uses category identifiers ( CATIDs).

The category manager uses an internal table, accessed with keys called GUID atoms to cache the GUIDs. Access to GUIDs is efficient using these atoms. When a GUID is obtained using its atom, the GUID description and value can be obtained from the Windows registry.

## -inheritance

The <b>ITfCategoryMgr</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCategoryMgr</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
