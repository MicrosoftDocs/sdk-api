---
UID: NF:fhcfg.IFhScopeIterator.GetItem
title: IFhScopeIterator::GetItem method
author: windows-driver-content
description: Retrieves the current item in an inclusion or exclusion list.
old-location: winprog\ifhscopeiterator_getitem.htm
old-project: DevNotes
ms.assetid: EB732725-497C-4D58-A05C-373732054BE5
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetItem method [Windows API], GetItem method [Windows API], IFhScopeIterator interface, GetItem,IFhScopeIterator.GetItem, IFhScopeIterator, IFhScopeIterator interface [Windows API], GetItem method, IFhScopeIterator::GetItem, fhcfg/IFhScopeIterator::GetItem, winprog.ifhscopeiterator_getitem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fhcfg.h
api_name:
-	IFhScopeIterator.GetItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFhScopeIterator::GetItem method


## -description


Retrieves the current item in an inclusion or exclusion list.


## -parameters




### -param Item [out]

This parameter must be <b>NULL</b> on input. On output, it receives a pointer to a string that contains the current element of the list. This element is a library name or a folder name, depending on the parameters that were passed to the <a href="https://msdn.microsoft.com/DE137C08-923D-4ADC-8EBC-2F277F72CAE4">IFhConfigMgr::GetIncludeExcludeRules</a> method. The string is allocated by calling <a href="https://msdn.microsoft.com/9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. You must call <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the string when it is no longer needed.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



To move to the next item in the inclusion or exclusion list, call the <a href="https://msdn.microsoft.com/FD8B5460-FBD7-47D3-ADB0-DB3D6AB5A51A">IFhScopeIterator::MoveToNextItem</a> method.




## -see-also




<a href="https://msdn.microsoft.com/E8F993BD-CB53-474A-926D-AED0F5A17073">IFhScopeIterator</a>



<a href="https://msdn.microsoft.com/FD8B5460-FBD7-47D3-ADB0-DB3D6AB5A51A">IFhScopeIterator::MoveToNextItem</a>
 

 

