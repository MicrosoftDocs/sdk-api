---
UID: NF:azroles.IAzBizRuleInterfaces.Remove
title: IAzBizRuleInterfaces::Remove method
author: windows-driver-content
description: Removes the specified interface from the list of interfaces The number of interfaces in the list of interfaces that can be called by BizRule scripts.
old-location: security\iazbizruleinterfaces_remove_method.htm
old-project: SecAuthZ
ms.assetid: 398e4151-aeda-48d0-b6f5-e0ea749d0720
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IAzBizRuleInterfaces, IAzBizRuleInterfaces interface [Security], Remove method, IAzBizRuleInterfaces::Remove, Remove method [Security], Remove method [Security], IAzBizRuleInterfaces interface, Remove,IAzBizRuleInterfaces.Remove, azroles/IAzBizRuleInterfaces::Remove, security.iazbizruleinterfaces_remove_method
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.h
api_name:
-	IAzBizRuleInterfaces.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzBizRuleInterfaces::Remove method


## -description


The <b>Remove</b> method removes the specified interface from the list of interfaces The number of interfaces in the list of interfaces that can be called by BizRule scripts.


## -parameters




### -param bstrInterfaceName [in]

The name of the interface to remove.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/063492b9-9970-4605-84f5-d8b80afc719b">AddInterface</a>



<a href="https://msdn.microsoft.com/96cc0e45-ddd5-4ab0-9243-5f2046e48f78">IAzBizRuleInterfaces</a>
 

 

