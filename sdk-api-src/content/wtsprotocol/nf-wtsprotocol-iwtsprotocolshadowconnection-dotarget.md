---
UID: NF:wtsprotocol.IWTSProtocolShadowConnection.DoTarget
title: IWTSProtocolShadowConnection::DoTarget
author: windows-sdk-content
description: IWTSProtocolShadowConnection::DoTarget is no longer available. Instead, use IWRdsProtocolShadowConnection::DoTarget.
old-location: termserv\iwtsprotocolshadowconnection_dotarget.htm
tech.root: TermServ
ms.assetid: 437983a4-48a4-4b37-99ba-35fe1f03b3ec
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DoTarget, DoTarget method [Remote Desktop Services], DoTarget method [Remote Desktop Services],IWTSProtocolShadowConnection interface, IWTSProtocolShadowConnection interface [Remote Desktop Services],DoTarget method, IWTSProtocolShadowConnection.DoTarget, IWTSProtocolShadowConnection::DoTarget, termserv.iwtsprotocolshadowconnection_dotarget, wtsprotocol/IWTSProtocolShadowConnection::DoTarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolShadowConnection.DoTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolShadowConnection::DoTarget


## -description


<p class="CCE_Message">[<b>IWTSProtocolShadowConnection::DoTarget</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/9fe2e3fb-f368-4b7e-b679-402db900916c">IWRdsProtocolShadowConnection::DoTarget</a>.]

Requests that the protocol start the target side of a shadow connection. 


## -parameters




### -param pParam1 [in]

A pointer to a byte that contains an arbitrary parameter.


### -param Param1Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam1</i> parameter.


### -param pParam2 [in]

A pointer to a byte that contains an arbitrary parameter.


### -param Param2Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam2</i> parameter.


### -param pParam3 [in]

A pointer to a byte that contains an arbitrary parameter.


### -param Param3Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam3</i> parameter.


### -param pParam4 [in]

A pointer to a byte that contains an arbitrary parameter.


### -param Param4Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam4</i> parameter.


### -param pClientName [in]

A pointer to a string that contains the name of the shadow client.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -remarks



The four parameters <i>pParam1</i>, <i>pParam2</i>, <i>pParam3</i>, and <i>pParam4</i> can contain any information that must be exchanged between the shadow client and the shadow target. The Remote Desktop Services service passes the information through without modification.




## -see-also




<a href="https://msdn.microsoft.com/83285a6a-903f-4c23-8f62-b04bbeaa52f9">IWTSProtocolShadowConnection</a>
 

 

