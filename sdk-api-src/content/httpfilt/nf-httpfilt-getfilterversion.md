---
UID: NF:httpfilt.GetFilterVersion
title: GetFilterVersion function
author: windows-driver-content
description: The GetFilterVersion function (if it is implemented) is the first entry-point function called by the Forefront TMG Web proxy to let a Web filter register for event notifications that are available to ISAPI filters in Internet Information Services (IIS).
old-location: tmg\getfilterversion.htm
old-project: TMG
ms.assetid: 9dcca0b7-e19e-4e8e-974f-fa70f1fd0b97
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetFilterVersion, GetFilterVersion callback function [Forefront TMG], httpfilt/GetFilterVersion, tmg.getfilterversion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: httpfilt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported,Forefront Threat Management Gateway (TMG) 2010
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 (64-bit only) [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: HTTP_VERSION, *PHTTP_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Httpfilt.h
api_name:
-	GetFilterVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# GetFilterVersion function


## -description


The <b>GetFilterVersion</b> function (if it is implemented) is the first entry-point function called by the Forefront TMG Web proxy to let a Web filter register for event notifications that are available to ISAPI filters in <a href="m_gly.htm">Internet Information Services (IIS)</a>. In the call, the Web proxy passes a pointer to an <a href="https://msdn.microsoft.com/070456a6-fbee-4660-bd8e-05ff54e04ba7">HTTP_FILTER_VERSION</a> data structure, which the Web filter can use to supply key filter configuration information to the Web proxy. The information passed to the Web proxy includes the version number of the Web filter API used by the Web filter and a bitmask containing flags that specify which event notifications the Web filter can process. This function must be implemented together with <a href="https://msdn.microsoft.com/15a44eb7-641b-4115-992e-6d08cb09be54">HttpFilterProc</a>.

To register for the notifications that are specific to Forefront TMG, use <a href="https://msdn.microsoft.com/83f874bc-5d2c-4a47-89b9-55230fbcce9d">GetWPXFilterVersion</a>. For more information about the types of event notifications that are sent to Web filters, see <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.

The declaratation of the <b>GetFilterVersion</b> function is:


## -parameters




### -param pVer [in, out]

Pointer to an <a href="https://msdn.microsoft.com/070456a6-fbee-4660-bd8e-05ff54e04ba7">HTTP_FILTER_VERSION</a> structure that contains a member which specifies the version information supplied by the Forefront TMG Web proxy and members which the Web filter uses to supply the version number of its Web filter API and a bitmask containing flags that specify the event notifications to be sent to it. The description field is not used in Forefront TMG.
						

The bitmask may include flags for the following event notifications that are available to ISAPI filters in IIS:

<ul>
<li>SF_NOTIFY_ACCESS_DENIED</li>
<li>SF_NOTIFY_AUTH_COMPLETE</li>
<li>SF_NOTIFY_AUTHENTICATION</li>
<li>SF_NOTIFY_END_OF_NET_SESSION</li>
<li>SF_NOTIFY_END_OF_REQUEST</li>
<li>SF_NOTIFY_LOG</li>
<li>SF_NOTIFY_PREPROC_HEADERS</li>
<li>SF_NOTIFY_READ_RAW_DATA</li>
<li>SF_NOTIFY_SEND_RAW_DATA</li>
<li>SF_NOTIFY_SEND_RESPONSE</li>
<li>SF_NOTIFY_URL_MAP</li>
</ul>
In addition to the flags for types of event notifications, flags relating to the port security of connections may be included in the bitmask:

<ul>
<li>SF_NOTIFY_SECURE_PORT</li>
<li>SF_NOTIFY_NONSECURE_PORT</li>
</ul>
<div class="alert"><b>Note</b>  The bitmask should not include the SF_NOTIFY_ORDER_LOW, SF_NOTIFY_ORDER_MEDIUM, and SF_NOTIFY_ORDER_HIGH flags that are used to set the priority of ISAPI extensions (filters). For a Web filter, the  priority is specified by the <a href="https://msdn.microsoft.com/3ebb984d-e75c-4db9-8333-ff1585bd493b">Priority</a> property of the <a href="https://msdn.microsoft.com/1960d3e9-a369-409e-b466-4fa42680c00c">FPCWebFilter</a> object that represents the filter. This property is initially set in the call to the <a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a> method of the <a href="https://msdn.microsoft.com/769cafa8-3f93-4dda-983a-a61e47d28978">FPCWebFilters</a> collection that creates the <b>FPCWebFilter</b> object in the filter registration code.</div>
<div> </div>

## -returns



If this function returns <b>TRUE</b>, the filter will remain loaded. If the function returns <b>FALSE</b>, the filter functionality will be terminated and the filter will be unloaded. If the function returns <b>FALSE</b> in your filter, the filter must call <a href="http://go.microsoft.com/fwlink/p/?linkid=21810">SetLastError</a> with an error code that indicates the nature of the failure.

<div class="alert"><b>Note</b>  It is important to register only for those notifications that are necessary for your filter's purposes. Registering for additional notifications will reduce performance.</div>
<div> </div>



## -remarks



At a minimum, a Web filter must implement either <b>GetFilterVersion</b> and <a href="https://msdn.microsoft.com/15a44eb7-641b-4115-992e-6d08cb09be54">HttpFilterProc</a>, or <a href="https://msdn.microsoft.com/83f874bc-5d2c-4a47-89b9-55230fbcce9d">GetWPXFilterVersion</a> and <a href="https://msdn.microsoft.com/d0d25ed4-2cc7-4dd3-ba89-07e7370909b4">HttpWPXFilterProc</a> (or both pairs of functions).




## -see-also




<a href="https://msdn.microsoft.com/371c9784-7d7a-4020-8e49-a8b6a72f2b5c">Entry-Point Functions</a>
 

 

