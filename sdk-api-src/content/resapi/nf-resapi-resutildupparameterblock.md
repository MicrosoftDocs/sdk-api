---
UID: NF:resapi.ResUtilDupParameterBlock
title: ResUtilDupParameterBlock function (resapi.h)
description: Performs a member-wise copy of the data from one parameter block to another.
helpviewer_keywords: ["PRESUTIL_DUP_PARAMETER_BLOCK","PRESUTIL_DUP_PARAMETER_BLOCK function [Failover Cluster]","ResUtilDupParameterBlock","ResUtilDupParameterBlock function [Failover Cluster]","_wolf_resutildupparameterblock","mscs.resutildupparameterblock","resapi/PRESUTIL_DUP_PARAMETER_BLOCK","resapi/ResUtilDupParameterBlock"]
old-location: mscs\resutildupparameterblock.htm
tech.root: MsCS
ms.assetid: b05b5afe-7d4b-4a21-9f28-88d6effaf5af
ms.date: 12/05/2018
ms.keywords: PRESUTIL_DUP_PARAMETER_BLOCK, PRESUTIL_DUP_PARAMETER_BLOCK function [Failover Cluster], ResUtilDupParameterBlock, ResUtilDupParameterBlock function [Failover Cluster], _wolf_resutildupparameterblock, mscs.resutildupparameterblock, resapi/PRESUTIL_DUP_PARAMETER_BLOCK, resapi/ResUtilDupParameterBlock
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilDupParameterBlock
 - resapi/ResUtilDupParameterBlock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilDupParameterBlock
---

# ResUtilDupParameterBlock function


## -description

Performs a member-wise copy of the data from one  <a href="/previous-versions/windows/desktop/mscs/parameter-blocks">parameter block</a> to another.

## -parameters

### -param pOutParams [out]

Pointer to the duplicated parameter block.

### -param pInParams [in]

Pointer to the original parameter block.

### -param pPropertyTable [in]

Pointer to an array of  <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a> structures describing properties in the original parameter block.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

<b>ResUtilDupParameterBlock</b> copies data only for parameter block members referenced in the <i>pPropertyTable</i> input parameter. If a variable in the input parameter block is a pointer, memory for the data is allocated with the function  <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>. You should deallocate this memory by calling either  <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> for each pointer variable in the output parameter block or  <a href="/windows/desktop/api/resapi/nf-resapi-resutilfreeparameterblock">ResUtilFreeParameterBlock</a>. Make sure that you deallocate memory whether  <b>ResUtilDupParameterBlock</b> succeeds or fails. For more information, see  <a href="/previous-versions/windows/desktop/mscs/using-parameter-blocks">Using Parameter Blocks</a> and  <a href="/previous-versions/windows/desktop/mscs/using-lists-and-tables">Using Lists and Tables</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfreeparameterblock">ResUtilFreeParameterBlock</a>