---
UID: NF:winddi.EngCreateDriverObj
title: EngCreateDriverObj function
author: windows-sdk-content
description: The EngCreateDriverObj function creates a DRIVEROBJ structure.
old-location: display\engcreatedriverobj.htm
old-project: display
ms.assetid: 2912a456-e5d7-4ae4-b8b0-d16c9e8eadf2
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: EngCreateDriverObj, EngCreateDriverObj function [Display Devices], display.engcreatedriverobj, gdifncs_b2ab33cf-bcdf-418d-87a5-eee4b0704433.xml, winddi/EngCreateDriverObj
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngCreateDriverObj
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngCreateDriverObj function


## -description


The <b>EngCreateDriverObj</b> function creates a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556162">DRIVEROBJ</a> structure. 


## -parameters




### -param pvObj

Pointer to the driver resource that will be tracked by the DRIVEROBJ structure. The resource is associated with the current client process.


### -param pFreeObjProc

Pointer to a driver-supplied callback function that frees the resource pointed to by <i>pvObj</i>. The callback function should be defined as follows, where <i>pDriverObj</i> points to the DRIVEROBJ structure:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>BOOL CALLBACK DrvobjFreeObjProc(DRIVEROBJ *pDriverObj);</pre>
</td>
</tr>
</table></span></div>

### -param hdev

Handle to the physical device associated with the object. This parameter is the GDI handle received by the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a> function.


## -returns



The return value is a handle that identifies the newly-created DRIVEROBJ structure if the function is successful. Otherwise, it is zero.




## -remarks



This structure is used to track a device-managed resource that must be released if the resource-allocating process terminates without first cleaning it up.

The driver can explicitly delete the DRIVEROBJ structure by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff564792">EngDeleteDriverObj</a>. Otherwise, the engine frees the resource by calling the function pointed to by <i>pFreeObjProc</i> when the process that created the DRIVEROBJ terminates.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556162">DRIVEROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564792">EngDeleteDriverObj</a>
 

 

