---
UID: NF:oleidl.IOleAdviseHolder.Unadvise
title: IOleAdviseHolder::Unadvise
author: windows-sdk-content
description: Deletes a previously established advisory connection.
old-location: com\ioleadviseholder_unadvise.htm
tech.root: com
ms.assetid: 620bc43f-dfc7-48b7-a574-ca7287ffa42f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOleAdviseHolder interface [COM],Unadvise method, IOleAdviseHolder.Unadvise, IOleAdviseHolder::Unadvise, Unadvise, Unadvise method [COM], Unadvise method [COM],IOleAdviseHolder interface, _ole_ioleadviseholder_unadvise, com.ioleadviseholder_unadvise, oleidl/IOleAdviseHolder::Unadvise
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
 - IOleAdviseHolder.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleAdviseHolder::Unadvise


## -description


Deletes a previously established advisory connection.


## -parameters




### -param dwConnection [in]

The value previously returned by <a href="https://msdn.microsoft.com/60bbb555-7d01-49cb-b7b3-9dc905066f94">IOleAdviseHolder::Advise</a> in <i>pdwConnection</i>.


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
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwConnection</i> parameter does not represent a valid advisory connection.

</td>
</tr>
</table>
 




## -remarks



<b>IOleAdviseHolder::Unadvise</b> is intended to be used to implement <a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">IOleObject::Unadvise</a> to delete an advisory connection. In general, you would use the OLE advise holder having obtained a pointer through a call to <a href="https://msdn.microsoft.com/f76e074e-6814-4735-9417-d5970e73089f">CreateOleAdviseHolder</a>.

Typically, containers call this method at shutdown or when an object is deleted. In certain cases, containers could call this method on objects that are running but not currently visible, as a way of reducing the overhead of maintaining multiple advisory connections.




## -see-also




<a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a>



<a href="https://msdn.microsoft.com/60bbb555-7d01-49cb-b7b3-9dc905066f94">IOleAdviseHolder::Advise</a>



<a href="https://msdn.microsoft.com/80a9ccd8-f89a-40c4-8b99-38536409cf26">IOleAdviseHolder::EnumAdvise</a>



<a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">IOleObject::Unadvise</a>
 

 

