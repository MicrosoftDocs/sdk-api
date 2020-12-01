---
UID: NF:objidl.IRunningObjectTable.IsRunning
title: IRunningObjectTable::IsRunning (objidl.h)
description: Determines whether the object identified by the specified moniker is currently running.
helpviewer_keywords: ["IRunningObjectTable interface [COM]","IsRunning method","IRunningObjectTable.IsRunning","IRunningObjectTable::IsRunning","IsRunning","IsRunning method [COM]","IsRunning method [COM]","IRunningObjectTable interface","_com_irunningobjecttable_isrunning","com.irunningobjecttable_isrunning","objidl/IRunningObjectTable::IsRunning"]
old-location: com\irunningobjecttable_isrunning.htm
tech.root: com
ms.assetid: 44564e70-b157-4f60-9b51-337613f6a4c9
ms.date: 12/05/2018
ms.keywords: IRunningObjectTable interface [COM],IsRunning method, IRunningObjectTable.IsRunning, IRunningObjectTable::IsRunning, IsRunning, IsRunning method [COM], IsRunning method [COM],IRunningObjectTable interface, _com_irunningobjecttable_isrunning, com.irunningobjecttable_isrunning, objidl/IRunningObjectTable::IsRunning
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRunningObjectTable::IsRunning
 - objidl/IRunningObjectTable::IsRunning
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IRunningObjectTable.IsRunning
---

# IRunningObjectTable::IsRunning


## -description

Determines whether the object identified by the specified moniker is currently running.

## -parameters

### -param pmkObjectName [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on the moniker.

## -returns

If the object is in the running state, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.

## -remarks

This method simply indicates whether a object is running. To retrieve a pointer to a running object, use the <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-getobject">IRunningObjectTable::GetObject</a> method.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Generally, you call the <b>IsRunning</b> method only if you are writing your own moniker class (that is, implementing the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface). You typically call this method from your implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-isrunning">IMoniker::IsRunning</a>. However, you should do so only if the <i>pmkToLeft</i> parameter of <b>IMoniker::IsRunning</b> is <b>NULL</b>. Otherwise, you should call <b>IMoniker::IsRunning</b> on your <i>pmkToLeft</i> parameter instead.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-isrunning">IMoniker::IsRunning</a>



<a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a>