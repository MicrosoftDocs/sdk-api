---
UID: NF:vpconfig.IVPBaseConfig.GetConnectInfo
title: IVPBaseConfig::GetConnectInfo
author: windows-sdk-content
description: The GetConnectInfo method retrieves information about the connections supported by the VPE object.
old-location: dshow\ivpbaseconfig_getconnectinfo.htm
tech.root: DirectShow
ms.assetid: b428e77a-83c3-42ce-95e4-1cdde4da066d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetConnectInfo, GetConnectInfo method [DirectShow], GetConnectInfo method [DirectShow],IVPBaseConfig interface, IVPBaseConfig interface [DirectShow],GetConnectInfo method, IVPBaseConfig.GetConnectInfo, IVPBaseConfig::GetConnectInfo, IVPBaseConfigGetConnectInfo, dshow.ivpbaseconfig_getconnectinfo, vpconfig/IVPBaseConfig::GetConnectInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Vpconfig.h
api_name:
 - IVPBaseConfig.GetConnectInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseConfig::GetConnectInfo


## -description



The <code>GetConnectInfo</code> method retrieves information about the connections supported by the VPE object.




## -parameters




### -param pdwNumConnectInfo [in, out]

Pointer to a variable that specifies the number of <b>DDVIDEOPORTCONNECT</b> structures in the <i>pddVPConnectInfo</i> array. On input, specifies the size of the array (in number of array elements). On output, contains the actual number of <b>DDVIDEOPORTCONNECT</b> structures that were copied into the array. If <i>pddVPConnectInfo</i> is <b>NULL</b>, the method returns the required array size.


### -param pddVPConnectInfo [in, out]

Pointer to an array of <b>DDVIDEOPORTCONNECT</b> structures, allocated by the caller. The device fills in the array with the connection information.


## -returns



Returns S_OK if successful, or an error code otherwise.




## -remarks



The client first calls this method with the value <b>NULL</b> for the <i>pddVPConnectInfo</i> parameter. The device returns the number of <b>DDVIDEOPORTCONNECT</b> structures in the <i>pdwNumConnectInfo</i> parameter. The client allocates an array of that size, and calls the method again, passing the address of the array in the <i>pddVPConnectInfo</i> parameter. The device copies the connection information into the buffer, and returns the actual number of copied structures in the <i>pdwNumConnectInfo</i> parameter.

The <b>DDVIDEOPORTCONNECT</b> structure is documented in the Windows DDK. The device can translate this method directly into an <i>DdVideoPortGetConnectInfo</i> call.

The client sets the connection information by calling the <a href="https://msdn.microsoft.com/e52bb213-e6e7-4bae-9e1e-6b34f34cf1d1">IVPBaseConfig::SetConnectInfo</a> method with an index number, which references one of the connection structures returned by this method.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 

