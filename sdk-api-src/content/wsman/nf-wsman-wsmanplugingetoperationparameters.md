---
UID: NF:wsman.WSManPluginGetOperationParameters
title: WSManPluginGetOperationParameters function
author: windows-driver-content
description: Gets operational information for items such as time-outs and data restrictions that are associated with the operation.
old-location: winrm\wsmanplugingetoperationparameters.htm
old-project: WinRM
ms.assetid: 338e7afc-d05b-4779-ae74-e9ee97e9e0ce
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: WSMAN_PLUGIN_PARAMS_GET_REQUESTED_DATA_LOCALE, WSMAN_PLUGIN_PARAMS_GET_REQUESTED_LOCALE, WSMAN_PLUGIN_PARAMS_LARGEST_RESULT_SIZE, WSMAN_PLUGIN_PARAMS_MAX_ENVELOPE_SIZE, WSMAN_PLUGIN_PARAMS_REMAINING_RESULT_SIZE, WSMAN_PLUGIN_PARAMS_TIMEOUT, WSManPluginGetOperationParameters, WSManPluginGetOperationParameters function [Windows Remote Management], winrm.wsmanplugingetoperationparameters, wsman/WSManPluginGetOperationParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSManSessionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WsmSvc.dll
api_name:
-	WSManPluginGetOperationParameters
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManPluginGetOperationParameters function


## -description


Gets operational information for items such as time-outs and data restrictions that are associated with the operation. A plug-in should not use these parameters for anything other than informational purposes.


## -parameters




### -param requestDetails [in]

A pointer to a <a href="https://msdn.microsoft.com/3191f2b3-e754-4f2d-ae8b-11da859c94b7">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.


### -param flags [in]

Specifies the options that are available for retrieval. This parameter must be set to either one of the following values or to a value defined by the plug-in.



#### WSMAN_PLUGIN_PARAMS_MAX_ENVELOPE_SIZE (1)

Specifies the maximum size of the operation response packet. The size includes the size of the data along with the Simple Object Access Protocol (SOAP)  overhead.

<div class="alert"><b>Note</b>  Some operations have a single call into the plug-in that can cause multiple roundtrips to occur. If no requests are waiting for data when this method is called, the maximum envelope size for the previous packet is given.</div>
<div> </div>


#### WSMAN_PLUGIN_PARAMS_TIMEOUT (2)

Specifies the time-out of the current operation.

<div class="alert"><b>Note</b>  Some operations have a single call into the plug-in that can cause multiple roundtrips to occur. If no requests are waiting for data when this method is called, the time-out for the previous packet is given.</div>
<div> </div>


#### WSMAN_PLUGIN_PARAMS_REMAINING_RESULT_SIZE (3)

Specifies how much space is left for data for the current operation. The size is based on the type of operation. For example, this flag would represent how large the single result item can be for a get operation. For enumerations, the size will decrease after each object is added. After the current packet has been filled with enumerations and get operations, it will be returned to the client even though more data is being accepted and cached.

<div class="alert"><b>Note</b>  Some operations have a single call into the plug-in that can cause multiple roundtrips to occur. If no requests are waiting for data when this method is called, the remaining size is given for a cached item.</div>
<div> </div>


#### WSMAN_PLUGIN_PARAMS_LARGEST_RESULT_SIZE (4)

Specifies the maximum size of the data for the current operation.



#### WSMAN_PLUGIN_PARAMS_GET_REQUESTED_LOCALE (5)

Specifies the language locale that was requested by the client for the operation.



#### WSMAN_PLUGIN_PARAMS_GET_REQUESTED_DATA_LOCALE (6)

Specifies the language locale of the data that was requested by the client.


### -param data [out]

A pointer to a <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a> structure that specifies the result object.


## -returns



The method returns <b>NO_ERROR</b> if it succeeded; otherwise,  it returns an error code. The following are the most common error codes:



