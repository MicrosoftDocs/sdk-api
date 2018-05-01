---
UID: NF:p2p.PeerCollabAddContact
title: PeerCollabAddContact function
author: windows-driver-content
description: Adds a contact to the contact list of a peer.
old-location: p2p\peercollabaddcontact.htm
old-project: P2PSdk
ms.assetid: 0e4ba039-2016-487d-b4df-e96648db1a05
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PeerCollabAddContact, PeerCollabAddContact function [Peer Networking], p2p.peercollabaddcontact, p2p/PeerCollabAddContact
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2P.dll
api_name:
-	PeerCollabAddContact
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerCollabAddContact function


## -description


The <b>PeerCollabAddContact</b> function adds a contact to the contact list of a peer.


## -parameters




### -param pwzContactData [in]

Pointer to a zero-terminated Unicode string buffer that contains the contact data for the peer that is added to the contact list. This string buffer can either be obtained by passing the peer name of the endpoint to add as a contact to <a href="https://msdn.microsoft.com/278c7622-988e-441d-a6b9-f62947f881e8">PeerCollabQueryContactData</a>, or through an out-of-band mechanism. 

To  send its own contact data out-of-band, the peer can call <a href="https://msdn.microsoft.com/8239e42f-3d86-416e-ad1b-93a37091811f">PeerCollabExportContact</a> with a <b>NULL</b> peer name. This function returns the contact data in XML format.


### -param ppContact [out, optional]

Pointer to a pointer to a <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structure. This parameter receives the address of a <b>PEER_CONTACT</b> structure containing peer contact information for the contact supplied in <i>pwzContactData</i>. This parameter may be <b>NULL</b>. 

Call <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a> on the address of the <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structure to free this data.


## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/8239e42f-3d86-416e-ad1b-93a37091811f">PeerCollabExportContact</a>



<a href="https://msdn.microsoft.com/278c7622-988e-441d-a6b9-f62947f881e8">PeerCollabQueryContactData</a>
 

 

