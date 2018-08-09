---
UID: NF:iads.IADsComputerOperations.Status
title: IADsComputerOperations::Status
author: windows-sdk-content
description: The IADsComputerOperations::Status method retrieves the status of a computer.
old-location: adsi\iadscomputeroperations_status.htm
old-project: ADSI
ms.assetid: 85243a67-3fe4-43f2-8173-4e9a507609ba
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsComputerOperations interface [ADSI],Status method, IADsComputerOperations.Status, IADsComputerOperations::Status, Status, Status method [ADSI], Status method [ADSI],IADsComputerOperations interface, _ds_iadscomputeroperations_status, adsi.iadscomputeroperations__status, adsi.iadscomputeroperations_status, iads/IADsComputerOperations::Status
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsComputerOperations.Status
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsComputerOperations::Status


## -description


The <b>IADsComputerOperations::Status</b> method retrieves the status of a computer.


## -parameters




### -param ppObject [out]

Pointer to an  <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface that reports the status code of computer operations. The status code is provider-specific.


## -returns



This method supports the standard return values as well as the following:

For other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>



<a href="https://msdn.microsoft.com/9b0155ce-f313-43fa-8605-650aa8f38587">IADsComputerOperations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

