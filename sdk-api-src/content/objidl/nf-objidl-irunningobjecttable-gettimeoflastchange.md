---
UID: NF:objidl.IRunningObjectTable.GetTimeOfLastChange
title: IRunningObjectTable::GetTimeOfLastChange (objidl.h)
description: Retrieves the time that an object was last modified.helpviewer_keywords: ["GetTimeOfLastChange","GetTimeOfLastChange method [COM]","GetTimeOfLastChange method [COM]","IRunningObjectTable interface","IRunningObjectTable interface [COM]","GetTimeOfLastChange method","IRunningObjectTable.GetTimeOfLastChange","IRunningObjectTable::GetTimeOfLastChange","_com_irunningobjecttable_gettimeoflastchange","com.irunningobjecttable_gettimeoflastchange","objidl/IRunningObjectTable::GetTimeOfLastChange"]
old-location: com\irunningobjecttable_gettimeoflastchange.htm
tech.root: com
ms.assetid: fef6f7e5-7d91-4737-98a4-c9779c6c2be5
ms.date: 12/05/2018
ms.keywords: GetTimeOfLastChange, GetTimeOfLastChange method [COM], GetTimeOfLastChange method [COM],IRunningObjectTable interface, IRunningObjectTable interface [COM],GetTimeOfLastChange method, IRunningObjectTable.GetTimeOfLastChange, IRunningObjectTable::GetTimeOfLastChange, _com_irunningobjecttable_gettimeoflastchange, com.irunningobjecttable_gettimeoflastchange, objidl/IRunningObjectTable::GetTimeOfLastChange
f1_keywords:
- objidl/IRunningObjectTable.GetTimeOfLastChange
dev_langs:
- c++
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
- IRunningObjectTable.GetTimeOfLastChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRunningObjectTable::GetTimeOfLastChange


## -description


Retrieves the time that an object was last modified.


## -parameters




### -param pmkObjectName [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on the moniker.


### -param pfiletime [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the object's last change time.



## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no entry for <i>pmkObjectName</i> in the ROT, or that the object it identifies is no longer running (in which case, the entry is revoked).

</td>
</tr>
</table>
 




## -remarks



This method returns the change time that was last reported for this object by a call to <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-notechangetime">IRunningObjectTable::NoteChangeTime</a>. If <b>NoteChangeTime</b> has not been called previously, the method returns the time that was recorded when the object was registered.

This method is provided to enable checking whether a connection between two objects (represented by one object holding a moniker that identifies the other) is up-to-date. For example, if one object is holding cached information about the other object, this method can be used to check whether the object has been modified since the cache was last updated. See <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imoniker-gettimeoflastchange">IMoniker::GetTimeOfLastChange</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Generally, you call <b>GetTimeOfLastChange</b> only if you are writing your own moniker class (that is, implementing the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface). You typically call this method from your implementation of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imoniker-gettimeoflastchange">IMoniker::GetTimeOfLastChange</a>. However, you should do so only if the <i>pmkToLeft</i> parameter of <b>IMoniker::GetTimeOfLastChange</b> is <b>NULL</b>. Otherwise, you should call <b>IMoniker::GetTimeOfLastChange</b> on your <i>pmkToLeft</i> parameter instead.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imoniker-gettimeoflastchange">IMoniker::GetTimeOfLastChange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a>
 

 

