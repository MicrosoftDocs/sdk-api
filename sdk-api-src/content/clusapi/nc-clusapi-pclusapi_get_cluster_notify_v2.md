---
UID: NC:clusapi.PCLUSAPI_GET_CLUSTER_NOTIFY_V2
title: PCLUSAPI_GET_CLUSTER_NOTIFY_V2
author: windows-driver-content
description: Retrieves information about the next notification event for a notification port.
old-location: mscs\getclusternotifyv2.htm
old-project: MsCS
ms.assetid: 0AF127E1-D517-4F4B-B797-40822B3B236F
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_GET_CLUSTER_NOTIFY_V2, PCLUSAPI_GET_CLUSTER_NOTIFY_V2 callback, PCLUSAPI_GET_CLUSTER_NOTIFY_V2 callback function [Failover Cluster], clusapi/PCLUSAPI_GET_CLUSTER_NOTIFY_V2, mscs.getclusternotifyv2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_GET_CLUSTER_NOTIFY_V2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_GET_CLUSTER_NOTIFY_V2 callback function


## -description


Retrieves information about the next notification event for a notification port.


## -parameters




### -param hChange [in]

A handle to the notification port. This handle is created by the 
      <a href="https://msdn.microsoft.com/81FE17A9-DE1C-4CDD-BE7D-50EA202D5AAC">CreateClusterNotifyPortV2</a> function.


### -param *lpdwNotifyKey [out]

A pointer to the notification key for the notification port.


### -param pFilterAndType [in, out, optional]

A  pointer to a <a href="https://msdn.microsoft.com/E173F5D8-955B-44FF-980E-CEF536A87AF5">NOTIFY_FILTER_AND_TYPE</a> 
      structure that describes the next notification event for the notification port.


### -param *buffer [in, out, optional]

A pointer to a buffer for the notification event.


### -param lpcchBufferSize


### -param lpszObjectId [in, out, optional]

A pointer to a  Unicode string   with  the ID of the 
       cluster object that triggered the event. The string ends with a  terminating null character.


### -param lpcchObjectId [in, out, optional]

On input, a pointer to a <b>DWORD</b> that specifies the maximum number of characters 
      that the <i>lpszObjectId</i> parameter can hold, including the terminating null character. On 
      output, a pointer to a <b>DWORD</b> that specifies the number of characters that 
      <i>lpszObjectId</i> received, excluding the terminating null character.


### -param lpszParentId [in, out, optional]

A pointer to a Unicode string with the ID of the parent to the cluster object that triggered the event. The 
      string ends with a terminating null character.


### -param lpcchParentId [in, out, optional]

On input, a pointer to a <b>DWORD</b> that specifies the maximum number of characters 
      the <i>lpszParentId</i> parameter can hold, including the terminating null character. On 
      output, a pointer to a <b>DWORD</b> that specifies the number of characters that 
      <i>lpszParentId</i> received, excluding the terminating null character.


### -param lpszName [in, out, optional]

A pointer to a Unicode string that contains the name of the cluster object that triggered the event. The 
      string ends with a terminating null character.


### -param lpcchName [in, out, optional]

On input, a pointer to a <b>DWORD</b> that specifies the maximum number of characters 
      that  the <i>lpszName</i> parameter can hold, including the terminating null character. On 
      output, a pointer to a <b>DWORD</b> that specifies the number of characters that 
      <i>lpszName</i> received, excluding the terminating null character.


### -param lpszType [in, out, optional]

A pointer to a  Unicode string that contains the type of  cluster object that triggered the event. The 
      string ends with a  terminating null character.


### -param lpcchType [in, out, optional]

On input, a pointer to a <b>DWORD</b> that specifies the maximum number of characters 
      the <i>lpszType</i> parameter can hold, including the terminating null character. On output, 
      a pointer to a <b>DWORD</b> that specifies the number of characters that 
      <i>lpszType</i> received, excluding the terminating null character.


### -param dwMilliseconds [in, optional]

A time-out value that specifies how long the caller is willing to wait for the notification.


#### - lpbBufferSize [in, out, optional]

A pointer to  the size of the <i>buffer</i> parameter, in bytes.


## -returns



if the operation succeeds,  this function returns  <b>ERROR_SUCCESS</b>.

If the operation fails, this function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Function</a>
 

 

