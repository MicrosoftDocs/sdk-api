---
UID: NF:oleidl.IOleObject.EnumAdvise
title: IOleObject::EnumAdvise
author: windows-sdk-content
description: Retrieves a pointer to an enumerator that can be used to enumerate the advisory connections registered for an object, so a container can know what to release prior to closing down.
old-location: com\ioleobject_enumadvise.htm
tech.root: com
ms.assetid: 4e1d6d9e-ebf2-4cd6-b7b4-00f9e7bd9bdc
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: EnumAdvise, EnumAdvise method [COM], EnumAdvise method [COM],IOleObject interface, IOleObject interface [COM],EnumAdvise method, IOleObject.EnumAdvise, IOleObject::EnumAdvise, _ole_ioleobject_enumadvise, com.ioleobject_enumadvise, oleidl/IOleObject::EnumAdvise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - OleIdl.h
api_name:
 - IOleObject.EnumAdvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleObject::EnumAdvise


## -description


Retrieves a pointer to an enumerator that can be used to enumerate the advisory connections registered for an object, so a container can know what to release prior to closing down.


## -parameters




### -param ppenumAdvise [out]

Address of <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> pointer variable that receives the interface pointer to the enumerator object. If the object does not have any advisory connections or if an error occurs, the implementation must set <i>ppenumAdvise</i> to <b>NULL</b>. Each time an object receives a successful call to <b>IOleObject::EnumAdvise</b>, it must increase the reference count on <i>ppenumAdvise</i>. It is the caller's responsibility to call Release when it is done with the <i>ppenumAdvise</i>.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/4e1d6d9e-ebf2-4cd6-b7b4-00f9e7bd9bdc">IOleObject::EnumAdvise</a> is not implemented.

</td>
</tr>
</table>
 




## -remarks



The <b>IOleObject::EnumAdvise</b> method supplies an enumerator that provides a way for containers to keep track of advisory connections registered for their objects. A container normally would call this function so that it can instruct an object to release each of its advisory connections prior to closing down.

The enumerator to which you get access through <b>IOleObject::EnumAdvise</b> enumerates items of type <a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a>. Upon receiving the pointer, the container can then loop through <b>STATDATA</b> and call <a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">IOleObject::Unadvise</a> for each enumerated connection.

The usual way to implement this function is to delegate the call to the <a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a> interface. Only the <b>pAdvise</b> and <b>dwConnection</b> members of <a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a> are relevant for <b>IOleObject::EnumAdvise</b>.




## -see-also




<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/6a68c9e9-6e06-4def-89a5-18e184e76a26">IOleObject::Advise</a>



<a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">IOleObject::Unadvise</a>
 

 

