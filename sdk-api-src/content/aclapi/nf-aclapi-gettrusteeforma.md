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

# GetTrusteeFormA function


## -description


The <b>GetTrusteeForm</b> function retrieves the trustee name from the specified <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure. This value indicates whether the structure uses a name string or a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) to identify the trustee.


## -parameters




### -param pTrustee [in]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


## -returns




						The return value is one of the constants from the 
<a href="https://msdn.microsoft.com/991ac6cb-3fc9-4915-b5c9-ae73efb25d68">TRUSTEE_FORM</a> enumeration.
					




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/9d3ce528-fb28-4e2e-bf7f-7d84c697fcb6">GetTrusteeName</a>



<a href="https://msdn.microsoft.com/19777929-43cf-45ea-8283-e42bf9ce8d7a">GetTrusteeType</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>



<a href="https://msdn.microsoft.com/991ac6cb-3fc9-4915-b5c9-ae73efb25d68">TRUSTEE_FORM</a>
 

 

