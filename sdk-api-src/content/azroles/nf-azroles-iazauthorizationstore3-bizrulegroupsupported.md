---
UID: NF:azroles.IAzAuthorizationStore3.BizruleGroupSupported
title: IAzAuthorizationStore3::BizruleGroupSupported
author: windows-sdk-content
description: Returns a Boolean value that specifies whether this IAzAuthorizationStore3 object supports application groups that use business rule (BizRule) scripts.
old-location: security\iazauthorizationstore3_bizrulegroupsupported_method.htm
tech.root: SecAuthZ
ms.assetid: 88449b12-5086-4f86-94d4-2a4afb4be070
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: BizruleGroupSupported, BizruleGroupSupported method [Security], BizruleGroupSupported method [Security],IAzAuthorizationStore3 interface, IAzAuthorizationStore3 interface [Security],BizruleGroupSupported method, IAzAuthorizationStore3.BizruleGroupSupported, IAzAuthorizationStore3::BizruleGroupSupported, azroles/IAzAuthorizationStore3::BizruleGroupSupported, security.iazauthorizationstore3_bizrulegroupsupported_method
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
 - IAzAuthorizationStore3.BizruleGroupSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzAuthorizationStore3::BizruleGroupSupported


## -description


The <b>BizruleGroupSupported</b> method returns a Boolean value that specifies whether this <a href="https://msdn.microsoft.com/en-us/library/Aa377594(v=VS.85).aspx">IAzAuthorizationStore3</a> object supports application groups that use business rule (BizRule) scripts.


## -parameters




### -param pbSupported [out]

<b>VARIANT_TRUE</b> if the current <a href="https://msdn.microsoft.com/en-us/library/Aa377594(v=VS.85).aspx">IAzAuthorizationStore3</a> object supports scripts that use business logic to determine group membership; otherwise, <b>VARIANT_FALSE</b>.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.



