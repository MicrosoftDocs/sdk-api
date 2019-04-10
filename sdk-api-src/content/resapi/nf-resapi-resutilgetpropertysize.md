---
UID: NF:resapi.ResUtilGetPropertySize
title: ResUtilGetPropertySize function (resapi.h)
author: windows-sdk-content
description: Returns the total number of bytes required for a specified property.
old-location: mscs\resutilgetpropertysize.htm
tech.root: MsCS
ms.assetid: 0f21ef2b-747c-4fb3-a13c-16bcb7bfd46e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_PROPERTY_SIZE, PRESUTIL_GET_PROPERTY_SIZE function [Failover Cluster], ResUtilGetPropertySize, ResUtilGetPropertySize function [Failover Cluster], _wolf_resutilgetpropertysize, mscs.resutilgetpropertysize, resapi/PRESUTIL_GET_PROPERTY_SIZE, resapi/ResUtilGetPropertySize
ms.topic: function
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilGetPropertySize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetPropertySize function


## -description


Returns the total number of bytes required for a specified property.


## -parameters




### -param hkeyClusterKey [in]


<a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">Cluster database</a> key identifying the location of the property to size.


### -param pPropertyTableItem [in]

Pointer to a  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structure describing the property to size.


### -param pcbOutPropertyListSize [in, out]

Pointer to the total number of bytes required for the property value, which includes the  <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure and the data.


### -param pnPropertyCount [in, out]

Pointer to the total number of properties. This value is incremented to include this property if  <b>ResUtilGetPropertySize</b> is successful.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The data type of a property specified in the property table does not match the data type of the same-named property stored in the cluster database.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>
 

 

