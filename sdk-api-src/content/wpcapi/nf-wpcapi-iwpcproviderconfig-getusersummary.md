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

# IWPCProviderConfig::GetUserSummary


## -description


Retrieves the information for each user by using the Parental Controls Control Panel. This interface is implemented by third parties.


## -parameters




### -param bstrSID [in]

A string that contains the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the user whose settings you want to obtain.


### -param pbstrUserSummary [out]

A pointer to a string that contains the summary details for the user specified in the <i>bstrSID</i> parameter.


## -returns



If the method succeeds, the function returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The user summary string is used to display information under each user in the Parental Controls Control Panel.




## -see-also




<a href="https://msdn.microsoft.com/008786aa-72ef-4591-8826-01176d3e3fba">IWPCProviderConfig</a>
 

 

