---
UID: NN:mfidl.IMFPMPServer
title: IMFPMPServer (mfidl.h)
description: Enables two instances of the Media Session to share the same protected media path (PMP) process.
helpviewer_keywords: ["IMFPMPServer","IMFPMPServer interface [Media Foundation]","IMFPMPServer interface [Media Foundation]","described","ba6dc70a-d77d-41de-afe1-65f2efcc4a95","mf.imfpmpserver","mfidl/IMFPMPServer"]
old-location: mf\imfpmpserver.htm
tech.root: mf
ms.assetid: ba6dc70a-d77d-41de-afe1-65f2efcc4a95
ms.date: 12/05/2018
ms.keywords: IMFPMPServer, IMFPMPServer interface [Media Foundation], IMFPMPServer interface [Media Foundation],described, ba6dc70a-d77d-41de-afe1-65f2efcc4a95, mf.imfpmpserver, mfidl/IMFPMPServer
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPMPServer
 - mfidl/IMFPMPServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPMPServer
---

# IMFPMPServer interface


## -description

Enables two instances of the <a href="/windows/desktop/medfound/media-session">Media Session</a> to share the same protected media path (PMP) process.

## -inheritance

The <b>IMFPMPServer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMPServer</b> also has these types of members:

## -remarks

If your application creates more than one instance of the Media Session, you can use this interface to share the same PMP process among several instances. This can be more efficient than re-creating the PMP process each time.

Use this interface as follows:

<ol>
<li>Create the first instance of the PMP Media Session by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession">MFCreatePMPMediaSession</a>.
          </li>
<li>Retrieve an <b>IMFPMPServer</b> pointer from the first Media Session by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier <b>MF_PMP_SERVER_CONTEXT</b>.
          </li>
<li>Create the second instance of the PMP Media Session. Set the <a href="/windows/desktop/medfound/mf-session-server-context-attribute">MF_SESSION_SERVER_CONTEXT</a> attribute on the <i>pConfiguration</i> parameter of the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession">MFCreatePMPMediaSession</a> function. The attribute value is the <b>IMFPMPServer</b> pointer retrieved in step 2.
          </li>
</ol>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>
