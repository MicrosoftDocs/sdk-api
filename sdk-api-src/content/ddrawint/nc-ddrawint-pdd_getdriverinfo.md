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

# PDD_GETDRIVERINFO callback function


## -description


The <i>DdGetDriverInfo</i> function queries the driver for additional DirectDraw and Direct3D functionality that the driver supports.


## -parameters




### -param Arg1








#### - lpGetDriverInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551550">DD_GETDRIVERINFODATA</a> structure that contains the information required to perform the query.


## -returns



<i>DdGetDriverInfo</i> must return DDHAL_DRIVER_HANDLED.




## -remarks



Drivers must implement <i>DdGetDriverInfo</i> to expose driver-supported DirectDraw functionality that is not returnable through <a href="https://msdn.microsoft.com/library/windows/hardware/ff556208">DrvEnableDirectDraw</a>.

The driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a> function returns a pointer to <i>DdGetDriverInfo</i> in the <b>GetDriverInfo</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551627">DD_HALINFO</a> structure.

To inform DirectDraw that the <b>GetDriverInfo</b> member has been set correctly, the driver must also set the DDHALINFO_GETDRIVERINFOSET bit of the <b>dwFlags</b> member in the DD_HALINFO structure. 

<i>DdGetDriverInfo</i> should determine whether the driver and its hardware support the callbacks or capabilities requested by the specified GUID. For all GUIDs except GUID_D3DParseUnknownCommandCallback, if the driver does provide the requested support, it should set the following members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551550">DD_GETDRIVERINFODATA</a> structure:

<ul>
<li>
Set <b>dwActualSize</b> to the size in bytes of the callback or capability structure being returned by the driver.

</li>
<li>In the memory that <b>lpvData</b> points to, initialize the members of the callback or capability structure that corresponds with the requested feature as follows:<ul>
<li>Set the <b>dwSize</b> member to the size in bytes of the structure.</li>
<li>For callbacks, set the function pointers to point to those callbacks implemented by the driver, and set the bits in the <b>dwFlags</b> member to indicate what functions the driver supports.</li>
<li>For capabilities, set the appropriate members of the capability structure with values supported by the driver/device.</li>
</ul>
</li>
<li>
Return DD_OK in <b>ddRVal</b>.

</li>
</ul>
If the driver does not support the feature, it should set <b>ddRVal</b> to DDERR_CURRENTLYNOTAVAIL and return.

DirectDraw informs the driver of the expected amount of data in the <b>dwExpectedSize</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551550">DD_GETDRIVERINFODATA</a> structure. The driver must not fill in more data than <b>dwExpectedSize</b> bytes.

To avoid problems using <i>DdGetDriverInfo</i>: 

<ul>
<li>
Do not implement dependencies based on the order in which <i>DdGetDriverInfo</i> is called. For example, avoid hooking driver initialization steps into <i>DdGetDriverInfo</i>. 

</li>
<li>
Do not try to ascertain the DirectDraw version based on the calls to <i>DdGetDriverInfo</i>. 

</li>
<li>
Do not assume anything about the number of times DirectDraw will call the driver, or the number of times DirectDraw will query a given GUID. It is possible that DirectDraw will probe the driver repeatedly with the same GUID. Implementing assumptions about this in the driver hampers its compatibility with future runtimes. 

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551550">DD_GETDRIVERINFODATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556208">DrvEnableDirectDraw</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a>
 

 

