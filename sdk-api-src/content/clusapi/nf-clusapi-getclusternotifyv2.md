---
UID: NF:clusapi.GetClusterNotifyV2
title: GetClusterNotifyV2 function (clusapi.h)
description: Retrieves information about the next notification event for a notification port.
helpviewer_keywords: ["GetClusterNotifyV2","GetClusterNotifyV2 function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_NOTIFY_V2","PCLUSAPI_GET_CLUSTER_NOTIFY_V2 function [Failover Cluster]","clusapi/GetClusterNotifyV2","clusapi/PCLUSAPI_GET_CLUSTER_NOTIFY_V2","mscs.getclusternotifyv2"]
old-location: mscs\getclusternotifyv2.htm
tech.root: MsCS
ms.assetid: 0AF127E1-D517-4F4B-B797-40822B3B236F
ms.date: 12/05/2018
ms.keywords: GetClusterNotifyV2, GetClusterNotifyV2 function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NOTIFY_V2, PCLUSAPI_GET_CLUSTER_NOTIFY_V2 function [Failover Cluster], clusapi/GetClusterNotifyV2, clusapi/PCLUSAPI_GET_CLUSTER_NOTIFY_V2, mscs.getclusternotifyv2
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetClusterNotifyV2
 - clusapi/GetClusterNotifyV2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - GetClusterNotifyV2
---

# GetClusterNotifyV2 function


## -description

Retrieves information about the next notification event for a notification port.

## -parameters

### -param hChange [in]

A handle to the notification port. This handle is created by the 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyportv2">CreateClusterNotifyPortV2</a> function.

### -param lpdwNotifyKey [out]

A pointer to the notification key for the notification port.

### -param pFilterAndType [in, out, optional]

A  pointer to a <a href="/windows/desktop/api/clusapi/ns-clusapi-notify_filter_and_type">NOTIFY_FILTER_AND_TYPE</a> 
      structure that describes the next notification event for the notification port.

### -param buffer [in, out, optional]

A pointer to a buffer for the notification event.

### -param lpbBufferSize [in, out, optional]

A pointer to  the size of the <i>buffer</i> parameter, in bytes.

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

## -returns

if the operation succeeds,  this function returns  <b>ERROR_SUCCESS</b>.

If the operation fails, this function returns one of the following 
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The handle that is represented in the <i>hChange</i> parameter is invalid or has been 
         closed by another thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_TIMEOUT</b></dt>
<dt>258 (0x102)</dt>
</dl>
</td>
<td width="60%">
The call timed out before the notification could be successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234 (0xEA)</dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the  <i>lpszName</i>  parameter is not big enough to hold the 
         result. The <i>lpcchName</i> parameter returns the number of characters in the result, 
         excluding the terminating null character.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Function</a>