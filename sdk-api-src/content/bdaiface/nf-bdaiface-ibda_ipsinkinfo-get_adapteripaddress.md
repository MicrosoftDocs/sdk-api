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

# IBDA_IPSinkInfo::get_AdapterIPAddress


## -description



This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        



The <b>get_AdapterIPAddress</b> method retrieves the IP address of the data that the IP Sink filter receives. This address is assigned by the system; it is not guaranteed to be the same for any two instances of the IP Sink filter.


## -parameters




### -param pbstrBuffer [out]

Pointer to a <b>BSTR</b> that receives the IP address. The returned string has the form <code>N.N.N.N</code>; for example, <code>3.0.0.0</code>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The caller must free the returned string, using the <b>SysFreeString</b> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/fbbe12ea-964a-4a83-ac0a-ac8808bd9a63">IBDA_IPSinkInfo Interface</a>
 

 

