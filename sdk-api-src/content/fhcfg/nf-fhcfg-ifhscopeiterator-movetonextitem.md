---
UID: NF:fhcfg.IFhScopeIterator.MoveToNextItem
title: IFhScopeIterator::MoveToNextItem
author: windows-sdk-content
description: Moves to the next item in the inclusion or exclusion list.
old-location: winprog\ifhscopeiterator_movetonextitem.htm
old-project: devnotes
ms.assetid: FD8B5460-FBD7-47D3-ADB0-DB3D6AB5A51A
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IFhScopeIterator interface [Windows API],MoveToNextItem method, IFhScopeIterator.MoveToNextItem, IFhScopeIterator::MoveToNextItem, MoveToNextItem, MoveToNextItem method [Windows API], MoveToNextItem method [Windows API],IFhScopeIterator interface, fhcfg/IFhScopeIterator::MoveToNextItem, winprog.ifhscopeiterator_movetonextitem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhScopeIterator.MoveToNextItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFhScopeIterator::MoveToNextItem


## -description


Moves to the next item in the inclusion or exclusion list.


## -parameters






## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



If the current item is the last item in the list, or if the list is empty, this method returns <code>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</code>.




## -see-also




<a href="https://msdn.microsoft.com/E8F993BD-CB53-474A-926D-AED0F5A17073">IFhScopeIterator</a>



<a href="https://msdn.microsoft.com/EB732725-497C-4D58-A05C-373732054BE5">IFhScopeIterator::GetItem</a>
 

 

