---
UID: NN:rend.ITDirectoryObject
title: ITDirectoryObject (rend.h)
description: The ITDirectoryObject interface is the common interface supported by all objects that can be added and deleted by using the ITDirectory interface.
helpviewer_keywords: ["ITDirectoryObject","ITDirectoryObject interface [TAPI 2.2]","ITDirectoryObject interface [TAPI 2.2]","described","_tapi3_itdirectoryobject","rend/ITDirectoryObject","tapi3.itdirectoryobject"]
old-location: tapi3\itdirectoryobject.htm
tech.root: tapi3
ms.assetid: a48644a4-43e2-4c52-84be-0cb5c49e6436
ms.date: 12/05/2018
ms.keywords: ITDirectoryObject, ITDirectoryObject interface [TAPI 2.2], ITDirectoryObject interface [TAPI 2.2],described, _tapi3_itdirectoryobject, rend/ITDirectoryObject, tapi3.itdirectoryobject
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITDirectoryObject
 - rend/ITDirectoryObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectoryObject
---

# ITDirectoryObject interface


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITDirectoryObject</b> interface is the common interface supported by all objects that can be added and deleted by using the 
<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a> interface. Changes made to this object will not take effect on the server until the 
<a href="/windows/desktop/api/rend/nf-rend-itdirectory-modifydirectoryobject">ITDirectory::ModifyDirectoryObject</a> method is called. The following methods create the 
<b>ITDirectoryObject</b> interface:


<a href="/windows/desktop/api/rend/nf-rend-ienumdirectoryobject-next">IEnumDirectoryObject::Next</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectory-get_directoryobjects">ITDirectory::get_DirectoryObjects</a>



<a href="/windows/desktop/api/rend/nf-rend-itrendezvous-createdirectoryobject">ITRendezvous::CreateDirectoryObject</a>

## -inheritance

The <b>ITDirectoryObject</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDirectoryObject</b> also has these types of members:

