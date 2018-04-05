---
UID: NF:faxcom.IFaxRoutingMethod.get_DeviceName
title: IFaxRoutingMethod::get_DeviceName method
author: windows-driver-content
description: The DeviceName property is a null-terminated string that contains the user-friendly display name for a fax port.
old-location: fax\_mfax_ifaxroutingmethod_get_devicename_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0tk5.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: FaxRoutingMethod object [Fax Service], get_DeviceName property, IFaxRoutingMethod, IFaxRoutingMethod::get_DeviceName, _mfax_ifaxroutingmethod_get_devicename, fax._mfax_ifaxroutingmethod_get_devicename, fax._mfax_ifaxroutingmethod_get_devicename_vb, get_DeviceName property [Fax Service], get_DeviceName property [Fax Service], FaxRoutingMethod object, get_DeviceName,IFaxRoutingMethod.get_DeviceName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	FaxRoutingMethod.get_DeviceName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRoutingMethod::get_DeviceName method


## -description


The <b>DeviceName</b> property is a null-terminated string that contains the user-friendly display name for a fax port. 

This property is read-only.


## -parameters


## -remarks



Note that it is possible for multiple fax ports to have the same user-friendly name. You can use the <a href="https://msdn.microsoft.com/bb18ef93-53db-4423-9ef1-34ab3161acba">DeviceId</a> property to uniquely identify a fax port.

<b>DeviceName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/bb18ef93-53db-4423-9ef1-34ab3161acba">DeviceId</a>



<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/4ae5aa09-2961-4823-8c39-0b0a5b0bdc81">FaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>
 

 

