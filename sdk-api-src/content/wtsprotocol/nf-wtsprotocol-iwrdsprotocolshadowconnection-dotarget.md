---
UID: NF:wtsprotocol.IWRdsProtocolShadowConnection.DoTarget
title: IWRdsProtocolShadowConnection::DoTarget
author: windows-sdk-content
description: Requests that the protocol start the target side of a shadow connection.
old-location: termserv\iwrdsprotocolshadowconnection_dotarget.htm
old-project: TermServ
ms.assetid: 9fe2e3fb-f368-4b7e-b679-402db900916c
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: DoTarget, DoTarget method [Remote Desktop Services], DoTarget method [Remote Desktop Services],IWRdsProtocolShadowConnection interface, IWRdsProtocolShadowConnection interface [Remote Desktop Services],DoTarget method, IWRdsProtocolShadowConnection.DoTarget, IWRdsProtocolShadowConnection::DoTarget, termserv.iwrdsprotocolshadowconnection_dotarget, wtsprotocol/IWRdsProtocolShadowConnection::DoTarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolShadowConnection.DoTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolShadowConnection::DoTarget


## -description


Requests that the protocol start the target side of a shadow connection.


## -parameters




### -param pParam1 [in]

A pointer to a buffer that contains an arbitrary parameter.


### -param Param1Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam1</i> parameter.


### -param pParam2 [in]

A pointer to a buffer that contains an arbitrary parameter.


### -param Param2Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam2</i> parameter.


### -param pParam3 [in]

A pointer to a buffer that contains an arbitrary parameter.


### -param Param3Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam3</i> parameter.


### -param pParam4 [in]

A pointer to a buffer that contains an arbitrary parameter.


### -param Param4Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam4</i> parameter.


### -param pClientName [in]

A pointer to a string that contains the name of the shadow client.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -remarks



The four parameters <i>pParam1</i>, <i>pParam2</i>, <i>pParam3</i>, and <i>pParam4</i> can contain any information that must be exchanged between the shadow client and the shadow target. The Remote Desktop Services service passes the information through without modification.




## -see-also




<a href="https://msdn.microsoft.com/d23c4902-4e61-45ff-8a49-62eea1b92d4a">IWRdsProtocolShadowConnection</a>
 

 

