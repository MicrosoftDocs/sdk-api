---
UID: NN:mfidl.IMFContentProtectionManager
title: IMFContentProtectionManager (mfidl.h)
description: Enables playback of protected content by providing the application with a pointer to a content enabler object.
helpviewer_keywords: ["0dba0384-eac7-456a-af9f-86eb944cdb2e","IMFContentProtectionManager","IMFContentProtectionManager interface [Media Foundation]","IMFContentProtectionManager interface [Media Foundation]","described","mf.imfcontentprotectionmanager","mfidl/IMFContentProtectionManager"]
old-location: mf\imfcontentprotectionmanager.htm
tech.root: mf
ms.assetid: 0dba0384-eac7-456a-af9f-86eb944cdb2e
ms.date: 12/05/2018
ms.keywords: 0dba0384-eac7-456a-af9f-86eb944cdb2e, IMFContentProtectionManager, IMFContentProtectionManager interface [Media Foundation], IMFContentProtectionManager interface [Media Foundation],described, mf.imfcontentprotectionmanager, mfidl/IMFContentProtectionManager
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFContentProtectionManager
 - mfidl/IMFContentProtectionManager
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
 - IMFContentProtectionManager
---

# IMFContentProtectionManager interface


## -description

Enables playback of protected content by providing the application with a pointer to a content enabler object.

Applications that play protected content should implement this interface.

## -inheritance

The <b>IMFContentProtectionManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFContentProtectionManager</b> also has these types of members:

## -remarks

A <i>content enabler</i> is an object that performs some action that is required to play a piece of protected content. For example, the action might be obtaining a DRM license. Content enablers expose the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a> interface, which defines a generic mechanism for content enabler. Content enablers are created inside the protected media path (PMP) process. However, they must be invoked from the application process. Therefore, the <b>IMFContentProtectionManager</b> interface provides a way for the PMP Media Session to notify the application.

To use this interface, do the following:

<ol>
<li>
Implement the interface in your application.

</li>
<li>
Create an attribute store by calling <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a>.

</li>
<li>
Set the <a href="/windows/desktop/medfound/mf-session-content-protection-manager-attribute">MF_SESSION_CONTENT_PROTECTION_MANAGER</a> attribute on the attribute store. The attribute value is a pointer to your <b>IMFContentProtectionManager</b> implementation.

</li>
<li>
Call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession">MFCreatePMPMediaSession</a> and pass the attribute store in the <i>pConfiguration</i> parameter.

</li>
</ol>
If the content requires a content enabler, the application's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent">BeginEnableContent</a> method is called. Usually this method called during the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology">IMFMediaSession::SetTopology</a> operation, before the Media Session raises the <a href="/windows/desktop/medfound/mesessiontopologyset">MESessionTopologySet</a> event. The application might receive multiple <b>BeginEnableContent</b> calls for a single piece of content. The MESessionTopologySet event signals that the content-enabling process is complete for the current topology. The <b>BeginEnableContent</b> method can also be called outside of the <b>SetTopology</b> operation, but less commonly.

Many content enablers send machine-specific data to the network, which can have privacy implications. One of the purposes of the <b>IMFContentProtectionManager</b> interface is to give applications an opportunity to display information to the user and enable users to opt in or out of the process.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
