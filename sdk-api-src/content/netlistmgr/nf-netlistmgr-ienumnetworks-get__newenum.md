---
UID: NF:netlistmgr.IEnumNetworks.get__NewEnum
title: IEnumNetworks::get__NewEnum method
author: windows-driver-content
description: The get_NewEnum property returns an automation enumerator object that you can use to iterate through the IEnumNetworks collection.
old-location: nla\ienumnetworks_get__newenum.htm
old-project: NLA
ms.assetid: ddff98c2-669d-4f8d-9584-b8590705c2f0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IEnumNetworks, IEnumNetworks interface [Network Awareness], get__NewEnum method, IEnumNetworks::get__NewEnum, get__NewEnum method [Network Awareness], get__NewEnum method [Network Awareness], IEnumNetworks interface, get__NewEnum,IEnumNetworks.get__NewEnum, netlistmgr/IEnumNetworks::get__NewEnum, nla.ienumnetworks_get__newenum
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Netlistmgr.h
api_name:
-	IEnumNetworks.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumNetworks::get__NewEnum method


## -description


The <b>get_NewEnum</b> property returns an automation enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/ce2b65e5-89fe-48c9-aa00-373406891d02">IEnumNetworks</a> collection. 


## -parameters




### -param ppEnumVar [out]

Contains the new instance of the implemented interface.


## -returns



Returns S_OK if the method succeeds.




## -remarks



In Microsoft Visual Basic and Microsoft C#, you do not need to use the corresponding _NewEnum property, because it is automatically used in the implementation of  the For Each loop (for each in Visual C#).




## -see-also




<a href="https://msdn.microsoft.com/ce2b65e5-89fe-48c9-aa00-373406891d02">IEnumNetworks</a>
 

 

