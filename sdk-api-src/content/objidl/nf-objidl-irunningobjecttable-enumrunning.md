---
UID: NF:objidl.IRunningObjectTable.EnumRunning
title: IRunningObjectTable::EnumRunning
author: windows-sdk-content
description: Creates and returns a pointer to an enumerator that can list the monikers of all the objects currently registered in the running object table (ROT).
old-location: com\irunningobjecttable_enumrunning.htm
tech.root: com
ms.assetid: 09ff0d05-627b-4e47-8534-25cd8735c6e5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumRunning, EnumRunning method [COM], EnumRunning method [COM],IRunningObjectTable interface, IRunningObjectTable interface [COM],EnumRunning method, IRunningObjectTable.EnumRunning, IRunningObjectTable::EnumRunning, _com_irunningobjecttable_enumrunning, com.irunningobjecttable_enumrunning, objidl/IRunningObjectTable::EnumRunning
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IRunningObjectTable.EnumRunning
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRunningObjectTable::EnumRunning


## -description


Creates and returns a pointer to an enumerator that can list the monikers of all the objects currently registered in the running object table (ROT).


## -parameters




### -param ppenumMoniker [out]

A pointer to an <a href="https://msdn.microsoft.com/c8dec22b-946d-48ae-9315-54d353f3b853">IEnumMoniker</a> pointer variable that receives the interface pointer to the new enumerator for the ROT. When successful, the implementation calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the enumerator; it is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. If an error occurs; the implementation sets *<i>ppenumMoniker</i> to <b>NULL</b>.


## -returns



This method can return the standard return values E_OUTOFMEMORY and S_OK.




## -remarks



<b>IRunningObjectTable::EnumRunning</b> must create and return a pointer to an <a href="https://msdn.microsoft.com/c8dec22b-946d-48ae-9315-54d353f3b853">IEnumMoniker</a> interface on an enumerator object. The standard enumerator methods can then be called to enumerate the monikers currently registered in the registry. The enumerator cannot be used to enumerate monikers that are registered in the ROT after the enumerator has been created.

The <b>EnumRunning</b> method is intended primarily for the use by the system in implementing the alert object table. Note that OLE 2 does not include an implementation of the alert object table.




## -see-also




<a href="https://msdn.microsoft.com/c8dec22b-946d-48ae-9315-54d353f3b853">IEnumMoniker</a>



<a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a>
 

 

