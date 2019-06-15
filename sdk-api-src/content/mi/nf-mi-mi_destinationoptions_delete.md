---
UID: NF:mi.MI_DestinationOptions_Delete
title: MI_DestinationOptions_Delete function (mi.h)
author: windows-sdk-content
description: Deletes the destination options structure created by using the MI_Application_NewDestinationOptions or MI_DestinationOptions_Clone function.
old-location: wmi_v2\mi_destinationoptions_delete.htm
tech.root: wmi_v2
ms.assetid: c4cc8622-1adb-4e91-877f-11a260ca4bd7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_Delete, MI_DestinationOptions_Delete function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_Delete, wmi_v2.mi_destinationoptions_delete
ms.topic: function
f1_keywords: ["mi/MI_DestinationOptions_Delete"]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_DestinationOptions_Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_DestinationOptions_Delete function


## -description


Deletes the destination options structure created by using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_clone">MI_DestinationOptions_Clone</a> function.


## -parameters




### -param options [in, out]

A pointer to the destination options structure to delete.

