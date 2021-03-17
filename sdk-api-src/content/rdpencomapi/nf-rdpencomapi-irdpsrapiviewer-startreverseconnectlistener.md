---
UID: NF:rdpencomapi.IRDPSRAPIViewer.StartReverseConnectListener
title: IRDPSRAPIViewer::StartReverseConnectListener (rdpencomapi.h)
description: Initiates a listener for accepting reverse connections from the sharer to the viewer, or obtains the connection string that the sharer uses to reverse connect to the viewer.
helpviewer_keywords: ["IRDPSRAPIViewer interface [RDP]","StartReverseConnectListener method","IRDPSRAPIViewer.StartReverseConnectListener","IRDPSRAPIViewer::StartReverseConnectListener","StartReverseConnectListener","StartReverseConnectListener method [RDP]","StartReverseConnectListener method [RDP]","IRDPSRAPIViewer interface","rdp.irdpsrapiviewer_startreverseconnectlistener","rdpencomapi/IRDPSRAPIViewer::StartReverseConnectListener"]
old-location: rdp\irdpsrapiviewer_startreverseconnectlistener.htm
tech.root: rdp
ms.assetid: 6e45e21f-f3a5-4a9e-9d63-45d7a1972114
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIViewer interface [RDP],StartReverseConnectListener method, IRDPSRAPIViewer.StartReverseConnectListener, IRDPSRAPIViewer::StartReverseConnectListener, StartReverseConnectListener, StartReverseConnectListener method [RDP], StartReverseConnectListener method [RDP],IRDPSRAPIViewer interface, rdp.irdpsrapiviewer_startreverseconnectlistener, rdpencomapi/IRDPSRAPIViewer::StartReverseConnectListener
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIViewer::StartReverseConnectListener
 - rdpencomapi/IRDPSRAPIViewer::StartReverseConnectListener
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIViewer.StartReverseConnectListener
---

# IRDPSRAPIViewer::StartReverseConnectListener


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiviewer">IRDPSRAPIViewer</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Initiates a listener for accepting reverse connections from the sharer to the viewer, or obtains the connection string that the sharer uses to reverse connect to the viewer.

## -parameters

### -param bstrConnectionString [in]

Type: <b>BSTR</b>

The connection string that the sharer will use to start the listener.

### -param bstrUserName [in]

Type: <b>BSTR</b>

The user name to use for authentication.

### -param bstrPassword [in]

Type: <b>BSTR</b>

The password to use for authentication.

### -param pbstrReverseConnectString [out]

Type: <b>BSTR*</b>

A pointer to a <b>BSTR</b> that receives the connection string that the sharer can use to reverse connect to the viewer by using the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-connecttoclient">IRDPSRAPISharingSession::ConnectToClient</a> method.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -remarks

This method is used to perform two separate operations:

<ul>
<li>The first is to allow the viewer to obtain the connection string that the sharer uses to reverse connect to the viewer. To do so, the <i>bstrConnectionString</i>, <i>bstrUserName</i>, and <i>bstrPassword</i> parameters must all be <b>NULL</b>. The viewer then sends this connection string to the sharer in an application-defined method, such as storing the connection string in a file and sharing the file with the sharer.</li>
<li>The second operation is to initiate a listener that will watch for reverse connect attempts from the sharer. For this operation, the <i>pbstrReverseConnectString</i> parameter must be <b>NULL</b>.</li>
</ul>
The normal sequence of events for this procedure is as follows:

<ol>
<li>The viewer obtains its connection string by calling the <b>StartReverseConnectListener</b> method, passing <b>NULL</b> for the <i>bstrConnectionString</i>, <i>bstrUserName</i>, and <i>bstrPassword</i> parameters.</li>
<li>The viewer initiates a reverse connect listener by calling the <b>StartReverseConnectListener</b> method, passing <b>NULL</b> for the <i>pbstrReverseConnectString</i> parameter and valid values for the <i>bstrConnectionString</i>, <i>bstrUserName</i>, and <i>bstrPassword</i> parameters.</li>
<li>The viewer sends the connection string obtained in step 1 to the sharer.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiviewer">IRDPSRAPIViewer</a>