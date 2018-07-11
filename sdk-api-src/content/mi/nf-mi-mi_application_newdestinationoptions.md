---
UID: NF:mi.MI_Application_NewDestinationOptions
title: MI_Application_NewDestinationOptions function
author: windows-sdk-content
description: Creates an MI_DestinationOptions object that can be used with the MI_Application_NewSession function.
old-location: wmi_v2\mi_application_newdestinationoptions.htm
old-project: wmi_v2
ms.assetid: efaa1244-7fe4-4484-b9ac-e7309e2012b6
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_Application_NewDestinationOptions, MI_Application_NewDestinationOptions function [Windows Management Infrastructure (MI)], mi/MI_Application_NewDestinationOptions, wmi_v2.mi_application_newdestinationoptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Application_NewDestinationOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Application_NewDestinationOptions function


## -description


Creates an <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object that can be used with the <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>  function.


## -parameters




### -param application [in]

Handle returned from <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a>.


### -param options [out]

Options container that is returned from this function.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



Destination options are used to store the configuration associated with connecting to the destination computer.  The available options can vary depending on the underlying protocol.  If the session and operations on that session just need to work with the current thread identity (or process if thread is not impersonating), then additional settings may not be needed.

Options must be closed by a call to <a href="https://msdn.microsoft.com/c4cc8622-1adb-4e91-877f-11a260ca4bd7">MI_DestinationOptions_Delete</a>.



