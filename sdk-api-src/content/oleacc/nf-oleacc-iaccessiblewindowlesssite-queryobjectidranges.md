---
UID: NF:oleacc.IAccessibleWindowlessSite.QueryObjectIdRanges
title: IAccessibleWindowlessSite::QueryObjectIdRanges (oleacc.h)
author: windows-sdk-content
description: Retrieves the object ID ranges that a particular windowless Microsoft ActiveX control has reserved.
old-location: winauto\uiauto_IAccessibleWindowlessSite_QueryObjectIdRanges.htm
tech.root: WinAuto
ms.assetid: 36663457-57B7-40D4-8A52-9C4E9B551E8E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAccessibleWindowlessSite interface [Windows Accessibility],QueryObjectIdRanges method, IAccessibleWindowlessSite.QueryObjectIdRanges, IAccessibleWindowlessSite::QueryObjectIdRanges, QueryObjectIdRanges, QueryObjectIdRanges method [Windows Accessibility], QueryObjectIdRanges method [Windows Accessibility],IAccessibleWindowlessSite interface, oleacc/IAccessibleWindowlessSite::QueryObjectIdRanges, winauto.uiauto_IAccessibleWindowlessSite_QueryObjectIdRanges
ms.topic: method
f1_keywords: ["oleacc/IAccessibleWindowlessSite.QueryObjectIdRanges"]
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessibleWindowlessSite.QueryObjectIdRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccessibleWindowlessSite::QueryObjectIdRanges


## -description


Retrieves the object ID ranges that a particular windowless Microsoft ActiveX control has reserved.  


## -parameters




### -param pRangesOwner [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler">IAccessibleHandler</a>*</b>

The control whose ranges are being queried. 


### -param psaRanges [out, optional]

Type: <b>SAFEARRAY**</b>

Receives the array of object ID ranges. The array contains a set of paired integers. For each pair, the first integer is the first object ID in the range, and the second integer is a count of object IDs in the range.  


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite">IAccessibleWindowlessSite</a>
 

 

