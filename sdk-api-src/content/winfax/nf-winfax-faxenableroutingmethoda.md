---
UID: NF:winfax.FaxEnableRoutingMethodA
title: FaxEnableRoutingMethodA function
author: windows-driver-content
description: The FaxEnableRoutingMethod function enables or disables a fax routing method for a specific fax device. A fax administration application typically calls this function for device management.
old-location: fax\_mfax_faxenableroutingmethod.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9ov8.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: FaxEnableRoutingMethod, FaxEnableRoutingMethod function [Fax Service], FaxEnableRoutingMethodA, FaxEnableRoutingMethodW, _mfax_faxenableroutingmethod, fax._mfax_faxenableroutingmethod, winfax/FaxEnableRoutingMethod, winfax/FaxEnableRoutingMethodA, winfax/FaxEnableRoutingMethodW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxEnableRoutingMethodW (Unicode) and FaxEnableRoutingMethodA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EVT_VARIANT, *PEVT_VARIANT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	WinFax.lib
-	WinFax.dll
api_name:
-	FaxEnableRoutingMethod
-	FaxEnableRoutingMethodA
-	FaxEnableRoutingMethodW
product: Windows
targetos: Windows
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxEnableRoutingMethodA function


## -description


The <b>FaxEnableRoutingMethod</b> function enables or disables a fax routing method for a specific fax device. A fax administration application typically calls this function for device management.


## -parameters




### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function.


### -param RoutingGuid [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest. 

                    

For information about fax routing methods, see <a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">About the Fax Routing Extension API</a>. For information about the relationship between routing methods and GUIDs, see <a href="https://msdn.microsoft.com/a2144af9-9101-478f-93b9-393101dc1936">Fax Routing Methods</a>.


### -param Enabled [in]

Type: <b>BOOL</b>

Specifies a Boolean variable that indicates whether the application is enabling or disabling the fax routing method specified by the <i>RoutingGuid</i> parameter. If this parameter is <b>TRUE</b>, the application is enabling the routing method; if this parameter is <b>FALSE</b>, the application is disabling the routing method.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or both of the <i>FaxPortHandle</i> or <i>RoutingGuid</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>RoutingGuid</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_PORT_SET</a> access is required.

</td>
</tr>
</table>
 




## -remarks



A fax client application can call the <b>FaxEnableRoutingMethod</b> function to enable a fax routing method for a particular fax device. It can also call the function to disable a routing method enabled by a prior call to <b>FaxEnableRoutingMethod</b> or by the fax service administration application. For more information, see <a href="https://msdn.microsoft.com/356dda5c-852e-46b7-8fa4-f3a0c62d65cb">Managing Fax Routing Data</a>.

Call the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function to obtain a valid port handle to specify in the <i>FaxPortHandle</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/1f78fed5-6b49-4946-8607-f1d7f9052aaa">FaxEnumRoutingMethods</a>



<a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a>



<a href="https://msdn.microsoft.com/c9220335-bb45-48b3-b303-b6ea10260952">FaxRouteMethod</a>
 

 

