---
UID: NF:azroles.IAzBizRuleInterfaces.GetInterfaceValue
title: IAzBizRuleInterfaces::GetInterfaceValue
author: windows-sdk-content
description: Gets the ID and flags of the interface that corresponds to the specified interface name.
old-location: security\iazbizruleinterfaces_getinterfacevalue_method.htm
tech.root: secauthz
ms.assetid: d5d12529-6ce8-4189-949b-210d8ec84084
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetInterfaceValue, GetInterfaceValue method [Security], GetInterfaceValue method [Security],IAzBizRuleInterfaces interface, IAzBizRuleInterfaces interface [Security],GetInterfaceValue method, IAzBizRuleInterfaces.GetInterfaceValue, IAzBizRuleInterfaces::GetInterfaceValue, azroles/IAzBizRuleInterfaces::GetInterfaceValue, security.iazbizruleinterfaces_getinterfacevalue_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
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
 - Azroles.h
api_name:
 - IAzBizRuleInterfaces.GetInterfaceValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzBizRuleInterfaces::GetInterfaceValue


## -description


The <b>GetInterfaceValue</b> method gets the ID and flags of the interface that corresponds to the specified interface name.


## -parameters




### -param bstrInterfaceName [in]

A string that contains the interface name.


### -param lInterfaceFlag [out]

A pointer to the flags associated with the interface name.


### -param varInterface [out]

A pointer to the ID associated with the interface name.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/063492b9-9970-4605-84f5-d8b80afc719b">AddInterface</a>



<a href="https://msdn.microsoft.com/96cc0e45-ddd5-4ab0-9243-5f2046e48f78">IAzBizRuleInterfaces</a>
 

 

