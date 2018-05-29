---
UID: NF:bdaiface.IBDA_ConditionalAccess.GetModuleUI
title: IBDA_ConditionalAccess::GetModuleUI
author: windows-sdk-content
description: The GetModuleUI method retrieves the URL for a user interface dialog.
old-location: mstv\ibda_conditionalaccess_getmoduleui.htm
old-project: mstv
ms.assetid: 5d1856d8-d2e6-4ab1-a1ce-7dcf9bc8bd39
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetModuleUI, GetModuleUI method [Microsoft TV Technologies], GetModuleUI method [Microsoft TV Technologies],IBDA_ConditionalAccess interface, IBDA_ConditionalAccess interface [Microsoft TV Technologies],GetModuleUI method, IBDA_ConditionalAccess.GetModuleUI, IBDA_ConditionalAccess::GetModuleUI, IBDA_ConditionalAccessGetModuleUI, bdaiface/IBDA_ConditionalAccess::GetModuleUI, mstv.ibda_conditionalaccess_getmoduleui
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bdaiface.h
api_name:
-	IBDA_ConditionalAccess.GetModuleUI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_ConditionalAccess::GetModuleUI


## -description


The <b>GetModuleUI</b> method retrieves the URL for a user interface dialog.


## -parameters




### -param byDialogNumber [in]

Specifies the dialog number.


### -param pbstrURL [out]

Pointer to a pointer variable that receives a pointer to a string containing the URL. When the string is no longer required, call the <b>SysFreeString</b> function to free it.


## -returns




            If the method succeeds, it returns S_OK. If it fails, it returns an error code.
          




## -see-also




<a href="https://msdn.microsoft.com/93bd3c38-2591-4d36-b296-5ad939487277">IBDA_ConditionalAccess Interface</a>
 

 

