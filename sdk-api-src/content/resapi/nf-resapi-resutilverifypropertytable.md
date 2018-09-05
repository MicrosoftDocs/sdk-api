---
UID: NF:resapi.ResUtilVerifyPropertyTable
title: ResUtilVerifyPropertyTable function
author: windows-sdk-content
description: Uses a property table to verify that a property list is correctly formatted.
old-location: mscs\resutilverifypropertytable.htm
old-project: mscs
ms.assetid: 5a079081-c11a-4f85-89d4-09a5e7fab29f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PRESUTIL_VERIFY_PROPERTY_TABLE, PRESUTIL_VERIFY_PROPERTY_TABLE function [Failover Cluster], ResUtilVerifyPropertyTable, ResUtilVerifyPropertyTable function [Failover Cluster], _wolf_resutilverifypropertytable, mscs.resutilverifypropertytable, resapi/PRESUTIL_VERIFY_PROPERTY_TABLE, resapi/ResUtilVerifyPropertyTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: resapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RESOURCE_EXIT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
 - Ext-MS-Win-Cluster-ResUtils-L1-1-1.dll
api_name:
 - ResUtilVerifyPropertyTable
product: Windows
targetos: Windows
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
req.product: ADAM
---

# ResUtilVerifyPropertyTable function


## -description


Uses a  <a href="https://msdn.microsoft.com/48591d73-606b-42b4-9711-4f7a84e9e971">property table</a> to verify that a <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> is correctly formatted.


## -parameters




### -param pPropertyTable [in]

Pointer to a property table describing the properties that will be validated in the property list.


### -param Reserved

This parameter is reserved for future use.


### -param bAllowUnknownProperties [in]

If <b>TRUE</b>, the function ignores all properties in the property list that are not included in the property table. If <b>FALSE</b>, any property in the property list that is not included in the property table causes the function to return <b>ERROR_INVALID_PARAMETER</b>.


### -param pInPropertyList [in]

Pointer to the input buffer containing the property list to validate.


### -param cbInPropertyListSize [in]

Size in bytes of the input buffer pointed to by <i>pInPropertyList</i>.


### -param pOutParams [out, optional]

Pointer to a parameter block.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>
 

 

