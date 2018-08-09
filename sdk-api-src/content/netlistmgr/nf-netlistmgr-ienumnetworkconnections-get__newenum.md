---
UID: NF:netlistmgr.IEnumNetworkConnections.get__NewEnum
title: IEnumNetworkConnections::get__NewEnum
author: windows-sdk-content
description: The get_NewEnum property returns an automation enumerator object that you can use to iterate through the IEnumNetworkConnections collection.
old-location: nla\ienumnetworkconnections_get__newenum.htm
old-project: nla
ms.assetid: 38b3a58e-6ed1-488e-b5b8-50043adae8cc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumNetworkConnections interface [Network Awareness],get__NewEnum method, IEnumNetworkConnections.get__NewEnum, IEnumNetworkConnections::get__NewEnum, get__NewEnum, get__NewEnum method [Network Awareness], get__NewEnum method [Network Awareness],IEnumNetworkConnections interface, netlistmgr/IEnumNetworkConnections::get__NewEnum, nla.ienumnetworkconnections_get__newenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - IEnumNetworkConnections.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumNetworkConnections::get__NewEnum


## -description


The <b>get_NewEnum</b> property returns an automation enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/f7e69ede-c567-4285-a017-096c94fb3fe4">IEnumNetworkConnections</a> collection. 


## -parameters




### -param ppEnumVar [out]

Contains the new instance of the implemented interface.


## -returns



Returns S_OK if the method succeeds.




## -remarks



In Microsoft Visual Basic and Microsoft C#, you do not need to use the corresponding _NewEnum property, because it is automatically used in the implementation of  the For Each loop (for each in Visual C#).




## -see-also




<a href="https://msdn.microsoft.com/f7e69ede-c567-4285-a017-096c94fb3fe4">IEnumNetworkConnections</a>
 

 

