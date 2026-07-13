---
UID: NF:oleacc.IAccessibleWindowlessSite.ReleaseObjectIdRange
title: IAccessibleWindowlessSite::ReleaseObjectIdRange (oleacc.h)
description: Releases an object ID range that was acquired by a previous call to the IAccessibleWindowlessSite::AcquireObjectIdRange method.
helpviewer_keywords: ["IAccessibleWindowlessSite interface [Windows Accessibility]","ReleaseObjectIdRange method","IAccessibleWindowlessSite.ReleaseObjectIdRange","IAccessibleWindowlessSite::ReleaseObjectIdRange","ReleaseObjectIdRange","ReleaseObjectIdRange method [Windows Accessibility]","ReleaseObjectIdRange method [Windows Accessibility]","IAccessibleWindowlessSite interface","oleacc/IAccessibleWindowlessSite::ReleaseObjectIdRange","winauto.uiauto_IAccessibleWindowlessSite_ReleaseObjectIdRange"]
old-location: winauto\uiauto_IAccessibleWindowlessSite_ReleaseObjectIdRange.htm
tech.root: WinAuto
ms.assetid: CC7AEE46-88BE-445C-A377-C9E8C2B505D3
ms.date: 12/05/2018
ms.keywords: IAccessibleWindowlessSite interface [Windows Accessibility],ReleaseObjectIdRange method, IAccessibleWindowlessSite.ReleaseObjectIdRange, IAccessibleWindowlessSite::ReleaseObjectIdRange, ReleaseObjectIdRange, ReleaseObjectIdRange method [Windows Accessibility], ReleaseObjectIdRange method [Windows Accessibility],IAccessibleWindowlessSite interface, oleacc/IAccessibleWindowlessSite::ReleaseObjectIdRange, winauto.uiauto_IAccessibleWindowlessSite_ReleaseObjectIdRange
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAccessibleWindowlessSite::ReleaseObjectIdRange
 - oleacc/IAccessibleWindowlessSite::ReleaseObjectIdRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessibleWindowlessSite.ReleaseObjectIdRange
---

# IAccessibleWindowlessSite::ReleaseObjectIdRange


## -description

Releases an object ID range that was acquired by a previous call to the <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange">IAccessibleWindowlessSite::AcquireObjectIdRange</a> method.

## -parameters

### -param rangeBase [in]

Type: <b>long</b>

The first object ID in the range of IDs to be released.

### -param pRangeOwner [in, optional]

Type: <b><a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler">IAccessibleHandler</a>*</b>

The windowless ActiveX control with which the range was associated when it was acquired.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To prevent mistakes when releasing object ranges, the system uses the <i>pControl</i> parameter to ensure that the range of object IDs being released actually belongs to the specified windowless control.

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite">IAccessibleWindowlessSite</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange">IAccessibleWindowlessSite::AcquireObjectIdRange</a>