---
UID: NF:objidl.IStorage.CopyTo
title: IStorage::CopyTo
author: windows-sdk-content
description: Copies the entire contents of an open storage object to another storage object.
old-location: stg\istorage_copyto.htm
tech.root: Stg
ms.assetid: 8b25b32b-f739-406a-96e8-dba687c7f055
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CopyTo, CopyTo method [Structured Storage], CopyTo method [Structured Storage],IStorage interface, IStorage interface [Structured Storage],CopyTo method, IStorage.CopyTo, IStorage::CopyTo, _stg_istorage_copyto, objidl/IStorage::CopyTo, stg.istorage_copyto
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage.CopyTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStorage::CopyTo


## -description


The <b>CopyTo</b> method copies the entire contents of an open storage object to another storage object.


## -parameters




### -param ciidExclude [in]

The number of elements in the array pointed to by <i>rgiidExclude</i>. If <i>rgiidExclude</i> is <b>NULL</b>, then <i>ciidExclude</i> is ignored.


### -param rgiidExclude [in]

An array of interface identifiers (IIDs) that either the caller knows about and does not want copied or that the storage object does not support, but whose state the caller will later explicitly copy. The array can include 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>, indicating that only stream objects are to be copied, and 
<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>, indicating that only storage objects are to be copied. An array length of zero indicates that only the state exposed by the 
<b>IStorage</b> object is to be copied; all other interfaces on the object are to be ignored. Passing <b>NULL</b> indicates that all interfaces on the object are to be copied.


### -param snbExclude [in]

A string name block (refer to 
<a href="https://msdn.microsoft.com/8428a820-3d8a-41e0-9955-d355440e2ebc">SNB</a>) that specifies a block of storage or stream objects that are not to be copied to the destination. These elements are not created at the destination. If <b>IID_IStorage</b> is in the <i>rgiidExclude</i> array, this parameter is ignored. This parameter may be <b>NULL</b>.


### -param pstgDest [in]

A pointer to the open storage object into which this storage object is to be copied. The destination storage object can be a different implementation of the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface from the source storage object. Thus, <b>IStorage::CopyTo</b> can use only publicly available methods of the destination storage object. If <i>pstgDest</i> is open in transacted mode, it can be reverted by calling its 
<a href="https://msdn.microsoft.com/d1b7626e-bad1-47b5-8bcd-3da3b05c53c4">IStorage::Revert</a> method.


## -returns



This method can return one of these values.




## -remarks



This method merges elements contained in the source storage object with those already present in the destination. The layout of the destination storage object may differ from the source storage object.

The copy process is recursive, invoking <b>IStorage::CopyTo</b> and 
<a href="https://msdn.microsoft.com/5bcd7da6-8bd5-4ab7-952f-f0a12e87f2d4">IStream::CopyTo</a> on the elements nested inside the source.

When copying a stream on top of an existing stream with the same name, the existing stream is first removed and then replaced with the source stream. When copying a storage on top of an existing storage with the same name, the existing storage is not removed. As a result, after the copy operation, the destination 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> contains older elements, unless they were replaced by newer ones with the same names.

A storage object may expose interfaces other than 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>, including 
<a href="https://msdn.microsoft.com/cf92c62f-ef65-46b1-8f41-f2b31ff52044">IRootStorage</a>, 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>, or 
<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>. The <i>rgiidExclude</i> parameter permits the exclusion of any or all of these additional interfaces from the copy operation.

A caller with a newer or more efficient copy of an existing substorage or stream object may want to exclude the current versions of these objects from the copy operation. The <i>snbExclude</i> and <i>rgiidExclude</i> parameters provide two ways of excluding a storage objects existing storages or streams.

<h3><a id="Note_to_Callers"></a><a id="note_to_callers"></a><a id="NOTE_TO_CALLERS"></a>Note to Callers</h3>
The most common way to use the <b>IStorage::CopyTo</b> method is to copy everything from the source to the destination, as in most full-save and save-as operations.

The following  example code shows how to copy everything  from the source storage object to the destination storage object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>pstg-&gt;CopyTo(0, Null, Null, pstgDest)</pre>
</td>
</tr>
</table></span></div>
<div class="alert"><b>Note</b>  To compact a document file, call <b>CopyTo</b> on the root storage object and copy to a new storage object.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/d9d33c64-edac-480f-b295-b2a06e51af2e">IStorage::MoveElementTo</a>



<a href="https://msdn.microsoft.com/d1b7626e-bad1-47b5-8bcd-3da3b05c53c4">IStorage::Revert</a>
 

 

