---
UID: NN:rend.ITDirectory
title: ITDirectory (rend.h)
description: The ITDirectory interface is exposed by the Directory object, which corresponds to a particular directory.
helpviewer_keywords: ["ITDirectory","ITDirectory interface [TAPI 2.2]","ITDirectory interface [TAPI 2.2]","described","_tapi3_itdirectory","rend/ITDirectory","tapi3.itdirectory"]
old-location: tapi3\itdirectory.htm
tech.root: tapi3
ms.assetid: 9ec8c0ed-2fed-4701-acb5-86b69c10f18c
ms.date: 12/05/2018
ms.keywords: ITDirectory, ITDirectory interface [TAPI 2.2], ITDirectory interface [TAPI 2.2],described, _tapi3_itdirectory, rend/ITDirectory, tapi3.itdirectory
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
 - ITDirectory
 - rend/ITDirectory
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
 - ITDirectory
---

# ITDirectory interface


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITDirectory</b> interface is exposed by the Directory object, which corresponds to a particular directory. This interface provides methods that get and set directory information, and provide access to a particular directory object, such a conference or user. The 
<a href="/windows/desktop/api/rend/nf-rend-itrendezvous-createdirectory">ITRendezvous::CreateDirectory</a> and 
<a href="/windows/desktop/api/rend/nf-rend-ienumdirectory-next">IEnumDirectory::Next</a> methods create the 
<b>ITDirectory</b> interface.

## -inheritance

The <b>ITDirectory</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDirectory</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/directory-controls">Directory Controls</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
