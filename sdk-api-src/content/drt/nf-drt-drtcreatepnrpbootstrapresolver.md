---
UID: NF:drt.DrtCreatePnrpBootstrapResolver
title: DrtCreatePnrpBootstrapResolver function (drt.h)
author: windows-sdk-content
description: DrtCreatePnrpBootstrapResolver.
old-location: p2p\drtcreatepnrpbootstrapresolver.htm
tech.root: P2PSdk
ms.assetid: 5bd64f10-abb8-4cba-8ebd-780a6a0c7074
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrtCreatePnrpBootstrapResolver, DrtCreatePnrpBootstrapResolver function [Peer Networking], drt/DrtCreatePnrpBootstrapResolver, p2p.drtcreatepnrpbootstrapresolver
ms.topic: function
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtCreatePnrpBootstrapResolver
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrtCreatePnrpBootstrapResolver function


## -description


The <b>DrtCreatePnrpBootstrapResolver</b> function creates a bootstrap resolver based on the Peer Name Resolution Protocol (PNRP).    


## -parameters




### -param fPublish [in]

If <b>TRUE</b>, the PeerName contained in <i>pwzPeerName</i> and passed with the PNRP Bootstrap Resolver is published by the local DRT using PNRP.  This node will be resolvable by other nodes using the PNRP bootstrap provider, and will assist other nodes attempting to bootstrap 


### -param pwzPeerName [in]

The name of the peer to search for in the PNRP cloud. This string has a maximum limit of 137 unicode characters


### -param pwzCloudName [in, optional]

The name of the cloud to search for in for the DRT corresponding to the MeshName. 

This string has a maximum limit of 256 unicode characters. If left blank the PNRP Bootstrap Provider will use all PNRP clouds available.


### -param pwzPublishingIdentity [in, optional]

The PeerIdentity that is publishing into the PNRP cloud utilized for bootstrapping. This string has a maximum limit of
137 unicode characters.
It is important to note that if <i>fPublish</i> is set to <b>TRUE</b>, the <i>PublishingIdentity</i> must be allowed to publish the PeerName specified.


### -param ppResolver [out]

A pointer to the created PNRP bootstrap resolver which is used in the <a href="https://msdn.microsoft.com/22408b8e-b114-43cd-8f84-3eaf8508f441">DRT_SETTINGS</a> structure.


## -returns



This function returns S_OK on success. Other possible values include:

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
The system cannot allocate memory for the provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwzPeerName</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_S_RETRY</b></dt>
</dl>
</td>
<td width="60%">
Underlying calls to <a href="https://msdn.microsoft.com/27d8d6ab-679d-4b7b-bf90-7b0859e7e048">PeerPnrpStartup</a> or <a href="https://msdn.microsoft.com/27a1b563-7bbe-4117-8bc3-19dd47360308">PeerIdentityGetCryptKey</a> return a transient error.  Try calling this function again.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  This function may also surface errors returned by underlying calls to <a href="https://msdn.microsoft.com/27d8d6ab-679d-4b7b-bf90-7b0859e7e048">PeerPnrpStartup</a> or <a href="https://msdn.microsoft.com/27a1b563-7bbe-4117-8bc3-19dd47360308">PeerIdentityGetCryptKey</a>.</div>
<div> </div>



## -remarks



The default PNRP Bootstrap Resolver created by this function is specific to the DRT it is created for. As a result it cannot be re-used across multiple DRTs.




## -see-also




<a href="https://msdn.microsoft.com/22408b8e-b114-43cd-8f84-3eaf8508f441">DRT_SETTINGS</a>



<a href="https://msdn.microsoft.com/0ff7bcc6-548b-475a-8a83-1ca50dbe333d">DrtDeletePnrpBootstrapResolver</a>
 

 

