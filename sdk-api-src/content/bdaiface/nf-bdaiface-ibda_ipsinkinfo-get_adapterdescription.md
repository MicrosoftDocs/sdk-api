---
UID: NF:bdaiface.IBDA_IPSinkInfo.get_AdapterDescription
title: IBDA_IPSinkInfo::get_AdapterDescription
author: windows-sdk-content
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
old-location: mstv\ibda_ipsinkinfo_get_adapterdescription.htm
tech.root: mstv
ms.assetid: 68b41304-2043-4cbf-8872-7f3d9f3b7a83
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_IPSinkInfo interface [Microsoft TV Technologies],get_AdapterDescription method, IBDA_IPSinkInfo.get_AdapterDescription, IBDA_IPSinkInfo::get_AdapterDescription, IBDA_IPSinkInfoget_AdapterDescription, bdaiface/IBDA_IPSinkInfo::get_AdapterDescription, get_AdapterDescription, get_AdapterDescription method [Microsoft TV Technologies], get_AdapterDescription method [Microsoft TV Technologies],IBDA_IPSinkInfo interface, mstv.ibda_ipsinkinfo_get_adapterdescription
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_IPSinkInfo.get_AdapterDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_IPSinkInfo::get_AdapterDescription


## -description



This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        



The <b>get_AdapterDescription</b> method retrieves the description of the network adapter.


## -parameters




### -param pbstrBuffer [out]

Pointer to a <b>BSTR</b> that receives the description.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The caller must free the returned string, using the <b>SysFreeString</b> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693378(v=VS.85).aspx">IBDA_IPSinkInfo Interface</a>
 

 

