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

# NetGetAadJoinInformation function


## -description


Retrieves the join information for the specified tenant. This function examines the join information for Microsoft Azure Active Directory and the work account that the current user added.


## -parameters




### -param pcszTenantId [in, optional]

The tenant identifier for the joined account. If the device
                       is not joined to Azure Active Directory (Azure AD), and the user currently logged into Windows added no Azure AD work accounts  for the specified tenant,
                       the buffer that the <i>ppJoinInfo</i> parameter points to  is set to NULL.

If the specified
                       tenant ID is NULL or empty, <i>ppJoinInfo</i> is set to the default
                       join account information, or NULL if the device is not joined to Azure AD and the current user added  no Azure AD work accounts.
                       
                       The default join account is one of the following:

<ul>
<li>The Azure AD account, if the device is joined to Azure AD.</li>
<li>The Azure AD work account that the current user added, if the device is not joined to Azure AD,
                       but the current user added a single Azure AD work account.</li>
<li>Any of the Azure AD work accounts that the current user added,  if the device is not joined to Azure AD, but the current user added multiple
                       Azure AD work accounts. The algorithm for selecting one of the work
                       accounts is not specified.</li>
</ul>

### -param ppJoinInfo [out]

The join information for the tenant that the <i>pcszTenantId</i> parameter specifies. If this parameter is NULL,  the device is not joined to Azure AD and the current user added no Azure AD work accounts. You must call
                     the <a href="https://msdn.microsoft.com/BDFB6179-4B8C-43E3-8D34-A2B470EA0D0B">NetFreeAadJoinInformation</a> function to free the memory allocated for
                     this structure.



## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/BDFB6179-4B8C-43E3-8D34-A2B470EA0D0B">NetFreeAadJoinInformation</a>
 

 

