---
UID: NF:objidl.IRunningObjectTable.IsRunning
title: IRunningObjectTable::IsRunning (objidl.h)
author: windows-sdk-content
description: Determines whether the object identified by the specified moniker is currently running.
old-location: com\irunningobjecttable_isrunning.htm
tech.root: com
ms.assetid: 44564e70-b157-4f60-9b51-337613f6a4c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRunningObjectTable interface [COM],IsRunning method, IRunningObjectTable.IsRunning, IRunningObjectTable::IsRunning, IsRunning, IsRunning method [COM], IsRunning method [COM],IRunningObjectTable interface, _com_irunningobjecttable_isrunning, com.irunningobjecttable_isrunning, objidl/IRunningObjectTable::IsRunning
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
 - IRunningObjectTable.IsRunning
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRunningObjectTable::IsRunning


## -description


Determines whether the object identified by the specified moniker is currently running.


## -parameters




### -param pmkObjectName [in]

A pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface on the moniker.


## -returns



If the object is in the running state, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.




## -remarks



This method simply indicates whether a object is running. To retrieve a pointer to a running object, use the <a href="https://msdn.microsoft.com/5d74b3ee-323d-43f9-8eab-0866432659de">IRunningObjectTable::GetObject</a> method.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Generally, you call the <b>IsRunning</b> method only if you are writing your own moniker class (that is, implementing the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface). You typically call this method from your implementation of <a href="https://msdn.microsoft.com/081b394c-1fe8-4519-999e-b3985a77bd9c">IMoniker::IsRunning</a>. However, you should do so only if the <i>pmkToLeft</i> parameter of <b>IMoniker::IsRunning</b> is <b>NULL</b>. Otherwise, you should call <b>IMoniker::IsRunning</b> on your <i>pmkToLeft</i> parameter instead.




## -see-also




<a href="https://msdn.microsoft.com/081b394c-1fe8-4519-999e-b3985a77bd9c">IMoniker::IsRunning</a>



<a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a>
 

 

