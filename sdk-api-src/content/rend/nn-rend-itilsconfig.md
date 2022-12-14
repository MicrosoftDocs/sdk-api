---
UID: NN:rend.ITILSConfig
title: ITILSConfig (rend.h)
description: The ITILSConfig interface allows configuration of the ILS directory.
helpviewer_keywords: ["ITILSConfig","ITILSConfig interface [TAPI 2.2]","ITILSConfig interface [TAPI 2.2]","described","_tapi3_itilsconfig","rend/ITILSConfig","tapi3.itilsconfig"]
old-location: tapi3\itilsconfig.htm
tech.root: tapi3
ms.assetid: 92a5624b-acf5-4280-9932-860fde53c6a0
ms.date: 12/05/2018
ms.keywords: ITILSConfig, ITILSConfig interface [TAPI 2.2], ITILSConfig interface [TAPI 2.2],described, _tapi3_itilsconfig, rend/ITILSConfig, tapi3.itilsconfig
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
 - ITILSConfig
 - rend/ITILSConfig
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
 - ITILSConfig
---

# ITILSConfig interface


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITILSConfig</b> interface allows configuration of the ILS directory. This interface is available only on Directory objects that return DT_ILS from 
<a href="/windows/desktop/api/rend/nf-rend-itdirectory-get_directorytype">ITDirectory::get_DirectoryType</a>. The 
<b>ITILSConfig</b> interface is created by calling <b>QueryInterface</b> on 
<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>.

## -inheritance

The <b>ITILSConfig</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITILSConfig</b> also has these types of members:

