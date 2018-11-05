---
UID: NF:resapi.ResUtilFreeParameterBlock
title: ResUtilFreeParameterBlock function
author: windows-sdk-content
description: Deallocates memory that has been allocated for a parameter block by ResUtilDupParameterBlock.
old-location: mscs\resutilfreeparameterblock.htm
tech.root: MsCS
ms.assetid: 2e884794-dbb7-47a8-8843-e9c030ce515d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PRESUTIL_FREE_PARAMETER_BLOCK, PRESUTIL_FREE_PARAMETER_BLOCK function [Failover Cluster], ResUtilFreeParameterBlock, ResUtilFreeParameterBlock function [Failover Cluster], _wolf_resutilfreeparameterblock, mscs.resutilfreeparameterblock, resapi/PRESUTIL_FREE_PARAMETER_BLOCK, resapi/ResUtilFreeParameterBlock
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Ext-MS-Win-Cluster-ResUtils-L1-1-1.dll
api_name:
 - ResUtilFreeParameterBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilFreeParameterBlock function


## -description


Deallocates memory that has been allocated for a  <a href="https://msdn.microsoft.com/fd77397b-36dd-4a20-b3f4-7dbbee1fd787">parameter block</a> by  <a href="https://msdn.microsoft.com/b05b5afe-7d4b-4a21-9f28-88d6effaf5af">ResUtilDupParameterBlock</a>.


## -parameters




### -param pOutParams [in, out]

Pointer to the parameter block to deallocate.


### -param pInParams [in]

Pointer to the parameter block to use as a reference.


### -param pPropertyTable [in]

Pointer to an array of  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structures describing the properties in the input parameter block.


## -returns



This function has no return values.




## -remarks



The  <b>ResUtilFreeParameterBlock</b> utility function deallocates any memory allocated to each member of <i>pOutParams</i>, subject to the following limitations:

<ul>
<li>It will only deallocate memory for members referenced in the <i>pPropertyTable</i> input parameter.</li>
<li>It will not deallocate memory that is pointed to by any member of <i>pInParams</i>.</li>
</ul>
Do not use this function with parameter blocks that have not been allocated with  <a href="https://msdn.microsoft.com/b05b5afe-7d4b-4a21-9f28-88d6effaf5af">ResUtilDupParameterBlock</a>.




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>



<a href="https://msdn.microsoft.com/b05b5afe-7d4b-4a21-9f28-88d6effaf5af">ResUtilDupParameterBlock</a>
 

 

