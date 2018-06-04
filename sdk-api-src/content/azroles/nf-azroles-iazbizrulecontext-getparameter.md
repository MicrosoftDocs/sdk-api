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

# IAzBizRuleContext::GetParameter


## -description


The <b>GetParameter</b> method gets the specified value from the <i>varParameterValues</i> parameter of the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">IAzClientContext::AccessCheck</a> method.


## -parameters




### -param bstrParameterName [in]

Name of the value to return. The name must match the name in one of the elements in the array passed into the <i>varParameterNames</i> parameter of the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. 

<div class="alert"><b>Important</b>  Users of VBScript must be aware that the comparison between this parameter and the names in the <i>varParameterNames</i> parameter is case sensitive.</div>
<div> </div>

### -param pvarParameterValue [out]

Parameter value from the <i>varParameterValues</i> parameter of the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method that corresponds to the name specified by the <i>bstrParameterName</i> parameter, if found; otherwise, <b>NULL</b>.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



