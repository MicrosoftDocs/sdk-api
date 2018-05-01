---
UID: NS:httpfilt._HTTP_FILTER_VERSION
title: "_HTTP_FILTER_VERSION"
author: windows-driver-content
description: The HTTP_FILTER_VERSION structure is used by the GetFilterVersion and GetWPXFilterVersion entry-point functions to set the filter version information and to specify the types of event notifications which are to be sent to a Web filter.
old-location: tmg\http_filter_version.htm
old-project: TMG
ms.assetid: 070456a6-fbee-4660-bd8e-05ff54e04ba7
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: "*PHTTP_FILTER_VERSION, HTTP_FILTER_VERSION, HTTP_FILTER_VERSION structure [Forefront TMG], PHTTP_FILTER_VERSION, PHTTP_FILTER_VERSION structure pointer [Forefront TMG], _HTTP_FILTER_VERSION, httpfilt/HTTP_FILTER_VERSION, httpfilt/PHTTP_FILTER_VERSION, tmg.http_filter_version"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: HTTP_FILTER_VERSION, *PHTTP_FILTER_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Httpfilt.h
api_name:
-	HTTP_FILTER_VERSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_FILTER_VERSION structure


## -description


The <b>HTTP_FILTER_VERSION</b> structure is used by the <a href="https://msdn.microsoft.com/9dcca0b7-e19e-4e8e-974f-fa70f1fd0b97">GetFilterVersion</a> and <a href="https://msdn.microsoft.com/83f874bc-5d2c-4a47-89b9-55230fbcce9d">GetWPXFilterVersion</a> entry-point functions to set the filter version information and to specify the types of event notifications which are to be sent to a Web filter.


## -struct-fields




### -field dwServerFilterVersion

The version number of the Web filter API used by the Forefront TMG computer. Set by the Forefront TMG Web proxy.


### -field dwFilterVersion

The version number of the Web filter API used by the Web filter. Set by the Web filter. The version used by your filter can be set to WPX_HTTP_FILTER_REVISION definition, which is defined in the Wpxhttpfilt.h header file.

The filter version is required. If the filter version number is higher than the version number of the Web filter API used by the Forefront TMG computer  in the <b>dwServerFilterVersion</b> parameter, the filter will not be loaded to avoid version issues.


### -field lpszFilterDesc

Not used in Forefront TMG.


### -field dwFlags

Bitmask containing flags that specify the types of event notifications which are to be sent to the Web filter and the port security of connections for which event notifications are sent. This bitmask is set by the Web filter. For a complete list of the possible flags and descriptions of the event notifications that they specify, see <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.
					

<div class="alert"><b>Note</b>  The SF_NOTIFY_ORDER_DEFAULT, SF_NOTIFY_ORDER_LOW, SF_NOTIFY_ORDER_MEDIUM, and SF_NOTIFY_ORDER_HIGH flags should not be included in this parameter. These flags are used in ISAPI extensions (filters) to set the filter priority. For a Web filter, the priority is specified by the <a href="https://msdn.microsoft.com/3ebb984d-e75c-4db9-8333-ff1585bd493b">Priority</a> property of the <a href="https://msdn.microsoft.com/1960d3e9-a369-409e-b466-4fa42680c00c">FPCWebFilter</a> object that represents the filter. This property is initially set in the call to the <a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a> method of the <a href="https://msdn.microsoft.com/769cafa8-3f93-4dda-983a-a61e47d28978">FPCWebFilters</a> collection that creates the <b>FPCWebFilter</b> object in the filter registration code.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/f6100648-ba45-496f-a339-97defa274888">Notification Structures</a>
 

 

