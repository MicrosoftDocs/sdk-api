---
UID: NS:wbemcli.tag_CompileStatusInfo
title: tag_CompileStatusInfo
author: windows-sdk-content
description: Describes an error for the IMofCompiler interface.
old-location: wmi\wbem_compile_status_info.htm
old-project: WmiSdk
ms.assetid: 94B3516F-2DDA-4C93-B48E-67D7FE357F4E
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: WBEM_COMPILE_STATUS_INFO, WBEM_COMPILE_STATUS_INFO structure [Windows Management Instrumentation], tag_CompileStatusInfo, wbemcli/tag_CompileStatusInfo, wmi.wbem_compile_status_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.typenames: WBEM_COMPILE_STATUS_INFO
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - WBEM_COMPILE_STATUS_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tag_CompileStatusInfo structure


## -description


Describes an error for the <a href="https://msdn.microsoft.com/5e01c7ac-7090-4cde-b836-01fa9d3f27f5">IMofCompiler</a> interface.


## -struct-fields




### -field lPhaseError

TBD



#### 0

no error



#### 1

parsing error



#### 2

argument error



#### 3

errors occurred while storing the data.


### -field hRes

The actual error code.


### -field ObjectNum

Object that is at fault.


### -field FirstLine

First line number of the object.


### -field LastLine

Last line number of the object.


### -field dwOutFlags

Reserved.


## -remarks



The   <i>ObjectNum</i>, <i>FirstLine</i>, and <i>LastLine</i> parameters only contain values for errors that relate to a particular class or instance in the file.




## -see-also




<a href="https://msdn.microsoft.com/7f3cc061-839e-49c2-a225-452719f155a9">CompileBuffer</a>



<a href="https://msdn.microsoft.com/caf13a5c-2aca-4acb-8210-909737bf1022">CompileFile</a>



<a href="https://msdn.microsoft.com/39c5d621-0cdf-44e2-9ec0-c68299e85cb7">CreateBMOF</a>



<a href="https://msdn.microsoft.com/5e01c7ac-7090-4cde-b836-01fa9d3f27f5">IMofCompiler</a>
 

 

