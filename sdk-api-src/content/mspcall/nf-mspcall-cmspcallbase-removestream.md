---
UID: NF:mspcall.CMSPCallBase.RemoveStream
title: CMSPCallBase::RemoveStream (mspcall.h)
description: (Interface RemoveStream) The RemoveStream method is called by the application to remove a stream from the call. (CMSPCallBase.RemoveStream)
helpviewer_keywords: ["CMSPCallBase interface [TAPI 2.2]","RemoveStream method","CMSPCallBase.RemoveStream","CMSPCallBase::RemoveStream","RemoveStream","RemoveStream method [TAPI 2.2]","RemoveStream method [TAPI 2.2]","CMSPCallBase interface","_tapi3_cmspcallbase_removestream","mspcall/CMSPCallBase::RemoveStream","tapi3.cmspcallbase_removestream"]
old-location: tapi3\cmspcallbase_removestream.htm
tech.root: tapi3
ms.assetid: 5e2b4261-ba0f-429a-aef5-974b2841bf0b
ms.date: 12/05/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],RemoveStream method, CMSPCallBase.RemoveStream, CMSPCallBase::RemoveStream, RemoveStream, RemoveStream method [TAPI 2.2], RemoveStream method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_removestream, mspcall/CMSPCallBase::RemoveStream, tapi3.cmspcallbase_removestream
req.header: mspcall.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CMSPCallBase::RemoveStream
 - mspcall/CMSPCallBase::RemoveStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallBase.RemoveStream
---

# CMSPCallBase::RemoveStream


## -description

(Interface 
<b>RemoveStream</b>) The 
<b>RemoveStream</b> method is called by the application to remove a stream from the call. Derived MSP call objects that do not want to allow applications to remove streams should override this to simply return TAPI_E_NOTSUPPORTED. (This is a good simplification strategy for many MSPs.) Derived call objects that do support removal of streams by the application should override this method to remove the stream object from the call object's list of streams and release the call's references to the stream. (Also  see the 
<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallmultigraph">CMSPCallMultiGraph</a> implementation.)

## -parameters

### -param pStream

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface to be removed.

## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallbase">CMSPCallBase</a>
