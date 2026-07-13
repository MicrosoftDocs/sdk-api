---
UID: NN:uiautomationclient.IUIAutomationTableItemPattern
title: IUIAutomationTableItemPattern (uiautomationclient.h)
description: Provides access to a child element in a container that supports IUIAutomationTablePattern.
helpviewer_keywords: ["IUIAutomationTableItemPattern","IUIAutomationTableItemPattern interface [Windows Accessibility]","IUIAutomationTableItemPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationTableItemPattern","uiauto_IUIAutomationTableItemPattern","uiautomationclient/IUIAutomationTableItemPattern","winauto.uiauto_IUIAutomationTableItemPattern"]
old-location: winauto\uiauto_IUIAutomationTableItemPattern.htm
tech.root: WinAuto
ms.assetid: 8e9948ec-7c31-45dd-ac9f-e9eafed9d2db
ms.date: 12/05/2018
ms.keywords: IUIAutomationTableItemPattern, IUIAutomationTableItemPattern interface [Windows Accessibility], IUIAutomationTableItemPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTableItemPattern, uiauto_IUIAutomationTableItemPattern, uiautomationclient/IUIAutomationTableItemPattern, winauto.uiauto_IUIAutomationTableItemPattern
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationTableItemPattern
 - uiautomationclient/IUIAutomationTableItemPattern
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationTableItemPattern
---

# IUIAutomationTableItemPattern interface


## -description

Provides access to a  child element in a container that supports <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtablepattern">IUIAutomationTablePattern</a>.

## -inheritance

The <b>IUIAutomationTableItemPattern</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationTableItemPattern</b> also has these types of members:

## -remarks

Elements that support this interface must also support <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationgriditempattern">IUIAutomationGridItemPattern</a>, to provide properties that are not specific to tables.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
