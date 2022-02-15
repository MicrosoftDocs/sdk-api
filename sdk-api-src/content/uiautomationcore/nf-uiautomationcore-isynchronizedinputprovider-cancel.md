---
UID: NF:uiautomationcore.ISynchronizedInputProvider.Cancel
title: ISynchronizedInputProvider::Cancel (uiautomationcore.h)
description: Cancels listening for input.
helpviewer_keywords: ["Cancel","Cancel method [Windows Accessibility]","Cancel method [Windows Accessibility]","ISynchronizedInputProvider interface","ISynchronizedInputProvider interface [Windows Accessibility]","Cancel method","ISynchronizedInputProvider.Cancel","ISynchronizedInputProvider::Cancel","uiauto.uiauto_ISynchronizedInputProvider_Cancel","uiauto_ISynchronizedInputProvider_Cancel","uiautomationcore/ISynchronizedInputProvider::Cancel","winauto.uiauto_ISynchronizedInputProvider_Cancel"]
old-location: winauto\uiauto_ISynchronizedInputProvider_Cancel.htm
tech.root: WinAuto
ms.assetid: 388fd113-ec66-4152-a42a-a485edcb9b80
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Windows Accessibility], Cancel method [Windows Accessibility],ISynchronizedInputProvider interface, ISynchronizedInputProvider interface [Windows Accessibility],Cancel method, ISynchronizedInputProvider.Cancel, ISynchronizedInputProvider::Cancel, uiauto.uiauto_ISynchronizedInputProvider_Cancel, uiauto_ISynchronizedInputProvider_Cancel, uiautomationcore/ISynchronizedInputProvider::Cancel, winauto.uiauto_ISynchronizedInputProvider_Cancel
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - ISynchronizedInputProvider::Cancel
 - uiautomationcore/ISynchronizedInputProvider::Cancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ISynchronizedInputProvider.Cancel
---

# ISynchronizedInputProvider::Cancel


## -description

Cancels listening for input.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the provider is currently listening for input, it should revert to normal operation.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-isynchronizedinputprovider">ISynchronizedInputProvider</a>
