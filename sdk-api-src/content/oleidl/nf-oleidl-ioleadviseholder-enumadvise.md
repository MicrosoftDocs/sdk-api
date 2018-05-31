---
UID: NF:oleidl.IOleAdviseHolder.EnumAdvise
title: IOleAdviseHolder::EnumAdvise
author: windows-sdk-content
description: Creates an enumerator that can be used to enumerate the advisory connections currently established for an object.
old-location: com\ioleadviseholder_enumadvise.htm
old-project: com
ms.assetid: 80a9ccd8-f89a-40c4-8b99-38536409cf26
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: EnumAdvise, EnumAdvise method [COM], EnumAdvise method [COM],IOleAdviseHolder interface, IOleAdviseHolder interface [COM],EnumAdvise method, IOleAdviseHolder.EnumAdvise, IOleAdviseHolder::EnumAdvise, _ole_ioleadviseholder_enumadvise, com.ioleadviseholder_enumadvise, oleidl/IOleAdviseHolder::EnumAdvise
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleAdviseHolder.EnumAdvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleAdviseHolder::EnumAdvise


## -description


Creates an enumerator that can be used to enumerate the advisory connections currently established for an object.


## -parameters




### -param ppenumAdvise [out]

A pointer to an <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> pointer variable that receives the interface pointer to the new enumerator. If this parameter is <b>NULL</b>, there are presently no advisory connections on the object, or an error occurred. The advise holder is responsible for incrementing the reference count on the <b>IEnumSTATDATA</b> pointer this method supplies. It is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when it is finished with the pointer.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The enumeration operation has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/80a9ccd8-f89a-40c4-8b99-38536409cf26">IOleAdviseHolder::EnumAdvise</a> is not implemented.

</td>
</tr>
</table>
 




## -remarks



<b>IOleAdviseHolder::EnumAdvise</b> creates an enumerator that can be used to enumerate an object's established advisory connections. The method supplies a pointer to the <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> interface on this enumerator. Advisory connection information for each connection is stored in the <a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a> structure, and the enumerator must be able to enumerate these structures.

For this method, the only relevant structure members are <b>pAdvise</b> and <b>dwConnection</b>. Other members contain data advisory information. When you call the enumeration methods, and while an enumeration is in progress, the effect of registering or revoking advisory connections on what is to be enumerated is undefined.




## -see-also




<a href="https://msdn.microsoft.com/0863d013-6f55-40ce-92d2-68bb0455a911">IDataAdviseHolder::EnumAdvise</a>



<a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a>



<a href="https://msdn.microsoft.com/60bbb555-7d01-49cb-b7b3-9dc905066f94">IOleAdviseHolder::Advise</a>



<a href="https://msdn.microsoft.com/620bc43f-dfc7-48b7-a574-ca7287ffa42f">IOleAdviseHolder::Unadvise</a>



<a href="https://msdn.microsoft.com/4e1d6d9e-ebf2-4cd6-b7b4-00f9e7bd9bdc">IOleObject::EnumAdvise</a>



<a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a>
 

 

