---
UID: NF:azroles.IAzClientContext.GetRoles
title: IAzClientContext::GetRoles
author: windows-sdk-content
description: Returns the roles for the client context.
old-location: security\iazclientcontext_getroles.htm
tech.root: SecAuthZ
ms.assetid: 753506cc-ed44-4795-90e5-c76010181d8a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AzClientContext object [Security],GetRoles method, GetRoles, GetRoles method [Security], GetRoles method [Security],AzClientContext object, GetRoles method [Security],IAzClientContext interface, IAzClientContext interface [Security],GetRoles method, IAzClientContext.GetRoles, IAzClientContext::GetRoles, azroles/IAzClientContext::GetRoles, security.iazclientcontext_getroles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzClientContext.GetRoles
 - AzClientContext.GetRoles
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzClientContext::GetRoles


## -description


The <b>GetRoles</b> method returns the roles for the client context.


## -parameters




### -param bstrScopeName [in, optional]

Name of the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object from which the roles returned in the <i>pvarRoleNames</i> parameter are applicable. If this property is <b>NULL</b>, the roles from the application scope are returned; otherwise, the roles from the specified scope are returned instead of the roles from the application scope.


### -param pvarRoleNames [out]

A pointer to a <b>VARIANT</b> used to return a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a>. Each element of the <b>SAFEARRAY</b> is a <b>VARIANT</b> of type <b>BSTR</b> that contains the name of a role to which the client belongs at the scope specified by the <i>bstrScopeName</i> parameter.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.




## -remarks



In JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



