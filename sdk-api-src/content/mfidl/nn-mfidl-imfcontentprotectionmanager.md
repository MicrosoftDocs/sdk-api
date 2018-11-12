---
UID: NN:mfidl.IMFContentProtectionManager
title: IMFContentProtectionManager
author: windows-sdk-content
description: Enables playback of protected content by providing the application with a pointer to a content enabler object.
old-location: mf\imfcontentprotectionmanager.htm
tech.root: medfound
ms.assetid: 0dba0384-eac7-456a-af9f-86eb944cdb2e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 0dba0384-eac7-456a-af9f-86eb944cdb2e, IMFContentProtectionManager, IMFContentProtectionManager interface [Media Foundation], IMFContentProtectionManager interface [Media Foundation],described, mf.imfcontentprotectionmanager, mfidl/IMFContentProtectionManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFContentProtectionManager interface


## -description


Enables playback of protected content by providing the application with a pointer to a content enabler object.

Applications that play protected content should implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFContentProtectionManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFContentProtectionManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFContentProtectionManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f422135-8e5f-41fb-a709-77636d1b451b">BeginEnableContent</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request to perform a content enabling action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10893a0c-5476-4b7d-aad7-845a4ba70335">EndEnableContent</a>
</td>
<td align="left" width="63%">
Ends an asynchronous request to perform a content enabling action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d06f752f-3f9a-4c7c-9c49-c886a675fe3a">RemoteBeginEnableContent</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/2f422135-8e5f-41fb-a709-77636d1b451b">BeginEnableContent</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa7a2b3a-5982-4fd8-b5de-7439fc374dfa">RemoteEndEnableContent</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/10893a0c-5476-4b7d-aad7-845a4ba70335">EndEnableContent</a>. (Not used by applications.)

</td>
</tr>
</table> 


## -remarks



A <i>content enabler</i> is an object that performs some action that is required to play a piece of protected content. For example, the action might be obtaining a DRM license. Content enablers expose the <a href="https://msdn.microsoft.com/45d02bd0-1104-47ec-8559-8cc51590fc62">IMFContentEnabler</a> interface, which defines a generic mechanism for content enabler. Content enablers are created inside the protected media path (PMP) process. However, they must be invoked from the application process. Therefore, the <b>IMFContentProtectionManager</b> interface provides a way for the PMP Media Session to notify the application.

To use this interface, do the following:

<ol>
<li>
Implement the interface in your application.

</li>
<li>
Create an attribute store by calling <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a>.

</li>
<li>
Set the <a href="https://msdn.microsoft.com/66482541-63d4-439b-862f-7507605af5d8">MF_SESSION_CONTENT_PROTECTION_MANAGER</a> attribute on the attribute store. The attribute value is a pointer to your <b>IMFContentProtectionManager</b> implementation.

</li>
<li>
Call <a href="https://msdn.microsoft.com/cb492e68-3d8a-49b2-8c0b-bee8065b53a8">MFCreatePMPMediaSession</a> and pass the attribute store in the <i>pConfiguration</i> parameter.

</li>
</ol>
If the content requires a content enabler, the application's <a href="https://msdn.microsoft.com/2f422135-8e5f-41fb-a709-77636d1b451b">BeginEnableContent</a> method is called. Usually this method called during the <a href="https://msdn.microsoft.com/ea5313f0-b0fd-4945-97a2-b3f17937294f">IMFMediaSession::SetTopology</a> operation, before the Media Session raises the <a href="https://msdn.microsoft.com/22a298b7-d32b-44ed-b0a1-4e0398ecfe04">MESessionTopologySet</a> event. The application might receive multiple <b>BeginEnableContent</b> calls for a single piece of content. The MESessionTopologySet event signals that the content-enabling process is complete for the current topology. The <b>BeginEnableContent</b> method can also be called outside of the <b>SetTopology</b> operation, but less commonly.

Many content enablers send machine-specific data to the network, which can have privacy implications. One of the purposes of the <b>IMFContentProtectionManager</b> interface is to give applications an opportunity to display information to the user and enable to user to opt in or out of the process.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

