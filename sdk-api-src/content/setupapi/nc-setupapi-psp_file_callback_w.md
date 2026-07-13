---
UID: NC:setupapi.PSP_FILE_CALLBACK_W
title: PSP_FILE_CALLBACK_W (setupapi.h)
description: The FileCallback callback function is used by a few setup functions. (Unicode)
helpviewer_keywords: ["FileCallback","PSP_FILE_CALLBACK","PSP_FILE_CALLBACK callback","PSP_FILE_CALLBACK callback function [Setup API]","PSP_FILE_CALLBACK_A","PSP_FILE_CALLBACK_W","_setupapi_psp_file_callback","setup.psp_file_callback","setupapi/PSP_FILE_CALLBACK"]
old-location: setup\psp_file_callback.htm
tech.root: setup
ms.assetid: 41eaa57a-e116-443c-93ee-397456a5c466
ms.date: 12/05/2018
ms.keywords: FileCallback, PSP_FILE_CALLBACK, PSP_FILE_CALLBACK callback, PSP_FILE_CALLBACK callback function [Setup API], PSP_FILE_CALLBACK_A, PSP_FILE_CALLBACK_W, _setupapi_psp_file_callback, setup.psp_file_callback, setupapi/PSP_FILE_CALLBACK
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSP_FILE_CALLBACK_W
 - setupapi/PSP_FILE_CALLBACK_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - setupapi.h
api_name:
 - PSP_FILE_CALLBACK
 - psp_file_callback_w
---

# PSP_FILE_CALLBACK_W callback function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<i>FileCallback</i> callback function is used by a few setup functions. The <b>PSP_FILE_CALLBACK</b> type defines a pointer to this callback function. <i>FileCallback</i> is a placeholder for the application-defined function name.

For more information, see 
<a href="/windows/desktop/SetupApi/notifications">Notifications</a>, 
<a href="/windows/desktop/SetupApi/creating-a-custom-queue-callback-routine">Creating a Custom Queue Callback Routine</a>, and 
<a href="/windows/desktop/SetupApi/creating-a-cabinet-callback-routine">Creating a Cabinet Callback Routine</a>.

## -parameters

### -param Context

The context information about the queue notification  that is returned to the callback function.

### -param Notification

The event that triggers the call to the callback function.

### -param Param1

The additional notification information. The value is dependent on the notification that is being returned.

### -param Param2

The additional notification information. The value is dependent on the notification that is being returned.

## -see-also

<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallfilea">SetupInstallFile</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallfileexa">SetupInstallFileEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallfrominfsectiona">SetupInstallFromInfSection</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupiteratecabineta">SetupIterateCabinet</a>
