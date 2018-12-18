---
UID: NF:netcon.NcIsValidConnectionName
title: NcIsValidConnectionName function
author: windows-sdk-content
description: The NcIsValidConnectionName function verifies if the passed in connection name is valid.
old-location: ics\ncisvalidconnectionname.htm
tech.root: ics
ms.assetid: 08fe9ba2-3314-45ff-8aea-742dd5b15560
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NcIsValidConnectionName, NcIsValidConnectionName function [ICS/ICF], ics.ncisvalidconnectionname, netcon/NcIsValidConnectionName
ms.topic: function
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Netshell.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netshell.dll
api_name:
 - NcIsValidConnectionName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NcIsValidConnectionName function


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>NcIsValidConnectionName</b> function verifies if the passed in connection name is valid.


## -parameters




### -param pszwName [in]

Connection name to check.


## -returns



<b>TRUE</b> if connection name is valid.




## -see-also




<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

