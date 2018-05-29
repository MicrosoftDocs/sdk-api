---
UID: NF:winbase.PowerClearRequest
title: PowerClearRequest function
author: windows-sdk-content
description: Decrements the count of power requests of the specified type for a power request object.
old-location: base\powerclearrequest.htm
old-project: Power
ms.assetid: 794248b1-5aa8-495e-aca6-1a1f35dc9c7f
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: PowerClearRequest, PowerClearRequest function, PowerRequestAwayModeRequired, PowerRequestDisplayRequired, PowerRequestExecutionRequired, PowerRequestSystemRequired, base.powerclearrequest, winbase/PowerClearRequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	kernel32.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
-	PowerClearRequest
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PowerClearRequest function


## -description


Decrements the count of power requests of the specified type for a power request object.


## -parameters




### -param PowerRequest [in]

A handle to a power request object.


### -param RequestType [in]

The power request type to be decremented. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PowerRequestDisplayRequired"></a><a id="powerrequestdisplayrequired"></a><a id="POWERREQUESTDISPLAYREQUIRED"></a><dl>
<dt><b>PowerRequestDisplayRequired</b></dt>
</dl>
</td>
<td width="60%">
The display remains on even if there is no user input for an extended period of time.

</td>
</tr>
<tr>
<td width="40%"><a id="PowerRequestSystemRequired"></a><a id="powerrequestsystemrequired"></a><a id="POWERREQUESTSYSTEMREQUIRED"></a><dl>
<dt><b>PowerRequestSystemRequired</b></dt>
</dl>
</td>
<td width="60%">
The system continues to run instead of entering sleep after a period of user inactivity.

</td>
</tr>
<tr>
<td width="40%"><a id="PowerRequestAwayModeRequired"></a><a id="powerrequestawaymoderequired"></a><a id="POWERREQUESTAWAYMODEREQUIRED"></a><dl>
<dt><b>PowerRequestAwayModeRequired</b></dt>
</dl>
</td>
<td width="60%">
The system enters away mode instead of sleep. In away mode, the system continues to run but turns off audio and video to give the appearance of sleep.

</td>
</tr>
<tr>
<td width="40%"><a id="PowerRequestExecutionRequired"></a><a id="powerrequestexecutionrequired"></a><a id="POWERREQUESTEXECUTIONREQUIRED"></a><dl>
<dt><b>PowerRequestExecutionRequired</b></dt>
</dl>
</td>
<td width="60%">
The calling process continues to run instead of being suspended or terminated by process lifetime management mechanisms. When and how long the process is allowed to run depends on the operating system and  power policy settings. 

When a <b>PowerRequestExecutionRequired</b> request is active, it implies <b>PowerRequestSystemRequired</b>.

The <b>PowerRequestExecutionRequired</b> request type can be used only by applications. Services cannot use this request type.

<b>Windows 7 and Windows Server 2008 R2:  </b>This request type is supported starting with Windows 8 and Windows Server 2012.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/2122bf00-9e6b-48ab-89b0-f53dd6804902">PowerCreateRequest</a>



<a href="https://msdn.microsoft.com/85249de8-5832-4f25-bbd9-3576cfd1caa0">PowerSetRequest</a>
 

 

