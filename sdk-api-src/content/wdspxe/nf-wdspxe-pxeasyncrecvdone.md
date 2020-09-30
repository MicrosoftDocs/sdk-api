---
UID: NF:wdspxe.PxeAsyncRecvDone
title: PxeAsyncRecvDone function (wdspxe.h)
description: Passes the results of processing the client request asynchronously. This function should be called only if the PxeProviderRecvRequest function returns ERROR_IO_PENDING.
helpviewer_keywords: ["PXE_BA_CUSTOM","PXE_BA_IGNORE","PXE_BA_NBP","PXE_BA_REJECTED","PxeAsyncRecvDone","PxeAsyncRecvDone function [Windows Deployment Services]","wds.pxeasyncrecvdone","wdspxe/PxeAsyncRecvDone"]
old-location: wds\pxeasyncrecvdone.htm
tech.root: wds
ms.assetid: c3f847fe-6a1d-41d6-9ed1-807b6234f409
ms.date: 12/05/2018
ms.keywords: PXE_BA_CUSTOM, PXE_BA_IGNORE, PXE_BA_NBP, PXE_BA_REJECTED, PxeAsyncRecvDone, PxeAsyncRecvDone function [Windows Deployment Services], wds.pxeasyncrecvdone, wdspxe/PxeAsyncRecvDone
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PxeAsyncRecvDone
 - wdspxe/PxeAsyncRecvDone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeAsyncRecvDone
---

# PxeAsyncRecvDone function


## -description

Passes the results of processing the client request asynchronously. This function should be called 
    only if the <a href="/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a> function 
    returns <b>ERROR_IO_PENDING</b>.

## -parameters

### -param hClientRequest [in]

Handle to the request received from the client.

### -param Action [in]

Specifies the action that the system should take for this client request. The following table lists the 
      possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_BA_NBP"></a><a id="pxe_ba_nbp"></a><dl>
<dt><b>PXE_BA_NBP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The provider replied to the client with a standard DHCP response packet that contains the path to the 
        Network Boot Program. Returning this action means that the provider successfully completed the client request 
        by calling the <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxesendreply">PxeSendReply</a> function at least 
        once.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_BA_CUSTOM"></a><a id="pxe_ba_custom"></a><dl>
<dt><b>PXE_BA_CUSTOM</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The provider replied to the client by using a custom response that does not conform to DHCP 
        specifications. Returning this action means that the provider successfully completed the client request by 
        calling the <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxesendreply">PxeSendReply</a> function at least once.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_BA_IGNORE"></a><a id="pxe_ba_ignore"></a><dl>
<dt><b>PXE_BA_IGNORE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The provider does not want to service the client request and the request should not be passed to the next 
        provider. All resources associated with the client request are released and the client request is ignored. 
        Providers can also use this value if they recognize the client but the request was malformed.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_BA_REJECTED"></a><a id="pxe_ba_rejected"></a><dl>
<dt><b>PXE_BA_REJECTED</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The provider does not want to service the client request. The system passes the request to the next 
        provider in the list of registered providers. If this was the last provider in the list, then all resources 
        associated with the client request are released and client request is ignored.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxesendreply">PxeSendReply</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>