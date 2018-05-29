---
UID: NS:p2p.peer_application_registration_info_tag
title: peer_application_registration_info_tag
author: windows-sdk-content
description: The PEER_APPLICATION_REGISTRATION_INFO structure contains peer application information for registration with the local computer.
old-location: p2p\peer_application_registration_info.htm
old-project: P2PSdk
ms.assetid: 64c9eb02-3235-4824-8de1-352b0a1ffbb4
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: "*PPEER_APPLICATION_REGISTRATION_INFO, PCPEER_APPLICATION_REGISTRATION_INFO, PCPEER_APPLICATION_REGISTRATION_INFO structure pointer [Peer Networking], PEER_APPLICATION_REGISTRATION_INFO, PEER_APPLICATION_REGISTRATION_INFO structure [Peer Networking], PPEER_APPLICATION_REGISTRATION_INFO, PPEER_APPLICATION_REGISTRATION_INFO structure pointer [Peer Networking], p2p.peer_application_registration_info, p2p/PCPEER_APPLICATION_REGISTRATION_INFO, p2p/PEER_APPLICATION_REGISTRATION_INFO, p2p/PPEER_APPLICATION_REGISTRATION_INFO, peer_application_registration_info_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: PEER_APPLICATION_REGISTRATION_INFO, *PPEER_APPLICATION_REGISTRATION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_APPLICATION_REGISTRATION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_application_registration_info_tag structure


## -description


The <b>PEER_APPLICATION_REGISTRATION_INFO</b> structure contains peer application information for registration with the local computer.


## -struct-fields




### -field application


<a href="https://msdn.microsoft.com/a219231b-75d0-47d3-8294-f1cc25b43d27">PEER_APPLICATION</a> structure that contains the specific peer application data.


### -field pwzApplicationToLaunch

Zero-terminated Unicode string that contains the local path to the executable peer application. Note that this data is for local use only and that this structure is never transmitted remotely.


### -field pwzApplicationArguments

Zero-terminated Unicode string that contains command-line arguments that must be supplied to the application when the application is launched. This data is for local use only. The PEER_APPLICATION_REGISTRATION_INFO  structure is never transmitted remotely.


### -field dwPublicationScope


<a href="https://msdn.microsoft.com/fecb9403-f790-4955-a879-fb3e6fbfe8ca">PEER_PUBLICATION_SCOPE</a> enumeration value that specifies the publication scope for this application registration information. The only valid value for this member is PEER_PUBLICATION_SCOPE_INTERNET.


## -remarks



An "application" is a set of software or software  components available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

A peer application has a GUID representing a single specific application. When an application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To deregister a peer's application, call <a href="https://msdn.microsoft.com/2479b726-20f1-4370-9fcf-f29cec44c3ec">PeerCollabUnregisterApplication</a> with this GUID.




## -see-also




<a href="https://msdn.microsoft.com/a219231b-75d0-47d3-8294-f1cc25b43d27">PEER_APPLICATION</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

