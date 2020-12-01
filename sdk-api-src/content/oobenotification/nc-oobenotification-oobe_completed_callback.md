---
UID: NC:oobenotification.OOBE_COMPLETED_CALLBACK
title: OOBE_COMPLETED_CALLBACK (oobenotification.h)
description: Application-defined callback function used with the RegisterWaitUntilOOBECompleted function.
helpviewer_keywords: ["OOBE_COMPLETED_CALLBACK","OOBE_COMPLETED_CALLBACK callback","OOBE_COMPLETED_CALLBACK callback function","oobenotification/OOBE_COMPLETED_CALLBACK","windowssetupandmigration.oobe_completed_callback"]
old-location: windowssetupandmigration\oobe_completed_callback.htm
tech.root: windowssetupandmigration
ms.assetid: 9786D6C3-82B1-4546-9BE9-7705AD3B7DBD
ms.date: 12/05/2018
ms.keywords: OOBE_COMPLETED_CALLBACK, OOBE_COMPLETED_CALLBACK callback, OOBE_COMPLETED_CALLBACK callback function, oobenotification/OOBE_COMPLETED_CALLBACK, windowssetupandmigration.oobe_completed_callback
req.header: oobenotification.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - OOBE_COMPLETED_CALLBACK
 - oobenotification/OOBE_COMPLETED_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Oobenotification.h
api_name:
 - OOBE_COMPLETED_CALLBACK
---

# OOBE_COMPLETED_CALLBACK callback function


## -description

Application-defined callback function used with the <a href="/previous-versions/windows/desktop/api/oobenotification/nf-oobenotification-registerwaituntiloobecompleted">RegisterWaitUntilOOBECompleted</a> function.

## -parameters

### -param CallbackContext

Pointer to the callback context. This is the value passed to the <a href="/previous-versions/windows/desktop/api/oobenotification/nf-oobenotification-registerwaituntiloobecompleted">RegisterWaitUntilOOBECompleted</a> function as the <i>CallbackContext</i> parameter.

## -remarks

Once the callback function has completed, <a href="/previous-versions/windows/desktop/api/oobenotification/nf-oobenotification-unregisterwaituntiloobecompleted">UnregisterWaitUntilOOBECompleted</a> should be called.