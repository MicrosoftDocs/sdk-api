---
UID: NF:objidl.IRunningObjectTable.NoteChangeTime
title: IRunningObjectTable::NoteChangeTime (objidl.h)
description: Records the time that a running object was last modified. The object must have previously been registered with the running object table (ROT). This method stores the time of last change in the ROT.
helpviewer_keywords: ["IRunningObjectTable interface [COM]","NoteChangeTime method","IRunningObjectTable.NoteChangeTime","IRunningObjectTable::NoteChangeTime","NoteChangeTime","NoteChangeTime method [COM]","NoteChangeTime method [COM]","IRunningObjectTable interface","_com_irunningobjecttable_notechangetime","com.irunningobjecttable_notechangetime","objidl/IRunningObjectTable::NoteChangeTime"]
old-location: com\irunningobjecttable_notechangetime.htm
tech.root: com
ms.assetid: 7bc410f8-3a39-478d-bc4d-adcd976f305b
ms.date: 12/05/2018
ms.keywords: IRunningObjectTable interface [COM],NoteChangeTime method, IRunningObjectTable.NoteChangeTime, IRunningObjectTable::NoteChangeTime, NoteChangeTime, NoteChangeTime method [COM], NoteChangeTime method [COM],IRunningObjectTable interface, _com_irunningobjecttable_notechangetime, com.irunningobjecttable_notechangetime, objidl/IRunningObjectTable::NoteChangeTime
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
 - IRunningObjectTable::NoteChangeTime
 - objidl/IRunningObjectTable::NoteChangeTime
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
 - IRunningObjectTable.NoteChangeTime
---

# IRunningObjectTable::NoteChangeTime


## -description

Records the time that a running object was last modified. The object must have previously been registered with the running object table (ROT). This method stores the time of last change in the ROT.

## -parameters

### -param dwRegister [in]

The identifier of the ROT entry of the changed object. This value was previously returned by <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-register">IRunningObjectTable::Register</a>.

### -param pfiletime [in]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the object's last change time.

## -returns

This method can return the standard return values E_INVALIDARG and S_OK.

## -remarks

The time recorded by this method can be retrieved by calling <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-gettimeoflastchange">IRunningObjectTable::GetTimeOfLastChange</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A moniker provider (hands out monikers identifying its objects to make them accessible to others) must call the <b>NoteChangeTime</b> method whenever its objects are modified. It must have previously called <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-register">IRunningObjectTable::Register</a> and stored the identifier returned by that method; it uses that identifier when calling <b>NoteChangeTime</b>.



The most common type of moniker provider is a compound-document link source. This includes server applications that support linking to their documents (or portions of a document) and container applications that support linking to embeddings within their documents. Server applications that do not support linking can also use the ROT to cooperate with container applications that support linking to embeddings. 



When an object is first registered in the ROT, the ROT records its last change time as the value returned by calling <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-gettimeoflastchange">IMoniker::GetTimeOfLastChange</a> on the moniker being registered.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-gettimeoflastchange">IMoniker::GetTimeOfLastChange</a>



<a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a>