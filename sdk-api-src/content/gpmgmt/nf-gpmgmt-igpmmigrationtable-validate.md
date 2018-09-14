---
UID: NF:gpmgmt.IGPMMigrationTable.Validate
title: IGPMMigrationTable::Validate
author: windows-sdk-content
description: Validates the migration table.
old-location: gpmc\igpmmigrationtable_validate.htm
tech.root: GPMC
ms.assetid: 1b442155-3dd7-4a74-ad33-db79114459ac
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GPMMigrationTable class [GPMC],Validate method, IGPMMigrationTable interface [GPMC],Validate method, IGPMMigrationTable.Validate, IGPMMigrationTable::Validate, Validate, Validate method [GPMC], Validate method [GPMC],GPMMigrationTable class, Validate method [GPMC],IGPMMigrationTable interface, gpmc.igpmmigrationtable_validate, gpmgmt/IGPMMigrationTable::Validate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMMigrationTable.Validate
 - GPMMigrationTable.Validate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMMigrationTable::Validate


## -description


Validates the migration table.


## -parameters




### -param ppResult [out]

Reference to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface. The <b>Result</b> property references whether the validation is successful. The <a href="https://msdn.microsoft.com/8570d40c-25c2-405c-b52a-dae6c0eb50e0">Status</a> property references the <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> that contains the validation errors or warnings.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object. The <b>Result</b> property references whether the validation was successful. The <a href="https://msdn.microsoft.com/8570d40c-25c2-405c-b52a-dae6c0eb50e0">Status</a> property references the <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">GPMStatusMsgCollection</a> that contains the validation errors or warnings.

<h3>VB</h3>
Returns a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object. The <b>Result</b> property references whether the validation was successful. The <a href="https://msdn.microsoft.com/8570d40c-25c2-405c-b52a-dae6c0eb50e0">Status</a> property references the <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">GPMStatusMsgCollection</a> that contains the validation errors or warnings.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMMigrationTable</a>
 

 

