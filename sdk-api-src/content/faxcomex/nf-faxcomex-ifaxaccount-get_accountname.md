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

# IFaxAccount::get_AccountName


## -description


Retrieves the name of a particular fax account on the server.

This property is read-only.


## -parameters


## -remarks



If the account is not in the local domain, the format of name returned  is &lt;domain_name&gt;\&lt;user_name&gt;.

If the account is in the domain but not on the server, the format name returned is &lt;computer_name&gt;\&lt;user_name&gt; where &lt;computer_name&gt; is the name of the server that holds the account.

If the account is on the same server as the fax server, just the &lt;user_name&gt; of the account is returned.




## -see-also




<a href="https://msdn.microsoft.com/85adc440-3dc8-47ce-aae8-dfb04f824b09">FaxAccount</a>



<a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a>
 

 

