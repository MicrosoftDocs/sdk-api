---
UID: NF:oleacc.IAccessibleWindowlessSite.ReleaseObjectIdRange
title: IAccessibleWindowlessSite::ReleaseObjectIdRange
author: windows-sdk-content
description: Releases an object ID range that was acquired by a previous call to the IAccessibleWindowlessSite::AcquireObjectIdRange method.
old-location: winauto\uiauto_IAccessibleWindowlessSite_ReleaseObjectIdRange.htm
tech.root: WinAuto
ms.assetid: CC7AEE46-88BE-445C-A377-C9E8C2B505D3
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAccessibleWindowlessSite interface [Windows Accessibility],ReleaseObjectIdRange method, IAccessibleWindowlessSite.ReleaseObjectIdRange, IAccessibleWindowlessSite::ReleaseObjectIdRange, ReleaseObjectIdRange, ReleaseObjectIdRange method [Windows Accessibility], ReleaseObjectIdRange method [Windows Accessibility],IAccessibleWindowlessSite interface, oleacc/IAccessibleWindowlessSite::ReleaseObjectIdRange, winauto.uiauto_IAccessibleWindowlessSite_ReleaseObjectIdRange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAccessibleWindowlessSite.ReleaseObjectIdRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibleWindowlessSite::ReleaseObjectIdRange


## -description


Releases an object ID range that was acquired by a previous call to the <a href="https://msdn.microsoft.com/EB8BAD4D-0C8F-4926-A1B4-383D03C3B0C4">IAccessibleWindowlessSite::AcquireObjectIdRange</a> method.


## -parameters




### -param rangeBase [in]

Type: <b>long</b>

The first object ID in the range of IDs to be released.


### -param pRangeOwner [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1b6b2c02-f3b5-4a8a-9388-b3833cd0cd44">IAccessibleHandler</a>*</b>

The windowless ActiveX control with which the range was associated when it was acquired.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To prevent mistakes when releasing object ranges, the system uses the <i>pControl</i> parameter to ensure that the range of object IDs being released actually belongs to the specified windowless control.  




## -see-also




<a href="https://msdn.microsoft.com/1ED23B39-231B-46A2-9FED-969A36DA8DD9">IAccessibleWindowlessSite</a>



<a href="https://msdn.microsoft.com/EB8BAD4D-0C8F-4926-A1B4-383D03C3B0C4">IAccessibleWindowlessSite::AcquireObjectIdRange</a>
 

 

