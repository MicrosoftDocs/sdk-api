---
UID: NF:oleacc.IAccessibleWindowlessSite.AcquireObjectIdRange
title: IAccessibleWindowlessSite::AcquireObjectIdRange (oleacc.h)
description: Acquires a range of object IDs from the control host and marks them as reserved by a specific windowless control.
helpviewer_keywords: ["AcquireObjectIdRange","AcquireObjectIdRange method [Windows Accessibility]","AcquireObjectIdRange method [Windows Accessibility]","IAccessibleWindowlessSite interface","IAccessibleWindowlessSite interface [Windows Accessibility]","AcquireObjectIdRange method","IAccessibleWindowlessSite.AcquireObjectIdRange","IAccessibleWindowlessSite::AcquireObjectIdRange","oleacc/IAccessibleWindowlessSite::AcquireObjectIdRange","winauto.uiauto_IAccessibleWindowlessSite_AcquireObjectIdRange"]
old-location: winauto\uiauto_IAccessibleWindowlessSite_AcquireObjectIdRange.htm
tech.root: WinAuto
ms.assetid: EB8BAD4D-0C8F-4926-A1B4-383D03C3B0C4
ms.date: 12/05/2018
ms.keywords: AcquireObjectIdRange, AcquireObjectIdRange method [Windows Accessibility], AcquireObjectIdRange method [Windows Accessibility],IAccessibleWindowlessSite interface, IAccessibleWindowlessSite interface [Windows Accessibility],AcquireObjectIdRange method, IAccessibleWindowlessSite.AcquireObjectIdRange, IAccessibleWindowlessSite::AcquireObjectIdRange, oleacc/IAccessibleWindowlessSite::AcquireObjectIdRange, winauto.uiauto_IAccessibleWindowlessSite_AcquireObjectIdRange
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
 - IAccessibleWindowlessSite::AcquireObjectIdRange
 - oleacc/IAccessibleWindowlessSite::AcquireObjectIdRange
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
 - IAccessibleWindowlessSite.AcquireObjectIdRange
---

# IAccessibleWindowlessSite::AcquireObjectIdRange


## -description

Acquires a range of object IDs from the control host and marks them as reserved by a specific windowless control.

## -parameters

### -param rangeSize [in]

The size of the object ID range that is being requested.

### -param pRangeOwner [in, optional]

The windowless control that is requesting the range.

### -param pRangeBase [out]

The first object ID in the acquired range.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To avoid using an object ID that belongs to another windowless control, a control should acquire an object ID range before calling the <a href="/windows/desktop/api/winuser/nf-winuser-notifywinevent">NotifyWinEvent</a> function.  A control should acquire enough object IDs for all of its contained accessible objects.  For example, a tree control with 100 children would reserve at least 101 object IDs, one for the root, and one for each child.  A tree control that is expected to grow would reserve as many object IDs as expected. If the tree control is expected to grow by several hundred children, it would reserve a range of 1000 IDs just to be safe.  



When the window that contains the Microsoft ActiveX control receives a [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) message with an <b>LPARAM</b> value (object ID) that is in a reserved range, it should call the <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid">IAccessibleHandler::AccessibleObjectFromID</a> method to get an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> object for that object ID.

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite">IAccessibleWindowlessSite</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange">IAccessibleWindowlessSite::ReleaseObjectIdRange</a>