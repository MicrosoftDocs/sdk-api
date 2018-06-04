---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



