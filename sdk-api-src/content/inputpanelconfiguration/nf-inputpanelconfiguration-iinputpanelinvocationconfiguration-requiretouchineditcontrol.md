---
UID: NF:inputpanelconfiguration.IInputPanelInvocationConfiguration.RequireTouchInEditControl
title: IInputPanelInvocationConfiguration::RequireTouchInEditControl (inputpanelconfiguration.h)
description: Requires an explicit user tap in an edit field before the touch keyboard invokes.
helpviewer_keywords: ["IInputPanelInvocationConfiguration interface [Windows Shell]","RequireTouchInEditControl method","IInputPanelInvocationConfiguration.RequireTouchInEditControl","IInputPanelInvocationConfiguration::RequireTouchInEditControl","RequireTouchInEditControl","RequireTouchInEditControl method [Windows Shell]","RequireTouchInEditControl method [Windows Shell]","IInputPanelInvocationConfiguration interface","inputpanelconfiguration/IInputPanelInvocationConfiguration::RequireTouchInEditControl","shell.iinputpanelinvocationconfiguration_requiretouchineditcontrol"]
old-location: shell\iinputpanelinvocationconfiguration_requiretouchineditcontrol.htm
tech.root: shell
ms.assetid: FAFF0DC8-DD18-47A2-B3BD-24A69B75A100
ms.date: 12/05/2018
ms.keywords: IInputPanelInvocationConfiguration interface [Windows Shell],RequireTouchInEditControl method, IInputPanelInvocationConfiguration.RequireTouchInEditControl, IInputPanelInvocationConfiguration::RequireTouchInEditControl, RequireTouchInEditControl, RequireTouchInEditControl method [Windows Shell], RequireTouchInEditControl method [Windows Shell],IInputPanelInvocationConfiguration interface, inputpanelconfiguration/IInputPanelInvocationConfiguration::RequireTouchInEditControl, shell.iinputpanelinvocationconfiguration_requiretouchineditcontrol
req.header: inputpanelconfiguration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inputpanelconfiguration.idl
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
 - IInputPanelInvocationConfiguration::RequireTouchInEditControl
 - inputpanelconfiguration/IInputPanelInvocationConfiguration::RequireTouchInEditControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - inputpanelconfiguration.h
api_name:
 - IInputPanelInvocationConfiguration.RequireTouchInEditControl
---

# IInputPanelInvocationConfiguration::RequireTouchInEditControl


## -description

Requires an explicit user tap in an edit field before the touch keyboard invokes.



## -returns

The <b>RequireTouchInEditControl</b> method always returns <b>S_OK</b>.

## -remarks

When the <b>RequireTouchInEditControl</b> method is called, all future focus changes require an explicit user tap in an edit field before the touch keyboard invokes. You can call the <b>RequireTouchInEditControl</b> method multiple times, but there's no way to undo the setting. 

This setting applies for any focus event that takes place to a window that is running in the process that called it. The <b>RequireTouchInEditControl</b> method doesn't affect owned windows in another process that have an ownership chain to the current process that called <b>RequireTouchInEditControl</b>. 

The <b>RequireTouchInEditControl</b> method always returns <b>S_OK</b>. If this API is used, then the <b>IsUIBusy</b> property has no effect. The two interaction models are essentially mutually exclusive.

The following code shows how to call the <b>RequireTouchInEditControl</b> method.


```cpp
#include <inputpanelconfiguration.h>
#include <inputpanelconfiguration_i.c>

IInputPanelInvocationConfiguration *pInputPanelInvocationConfiguration;
CoCreateInstance(CLSID_InputPanelConfiguration, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pInputPanelInvocationConfiguration));
pInputPanelInvocationConfiguration->RequireTouchInEditControl();

```


<div class="alert"><b>Note</b>  Calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> before the app finishes drawing UI can cause undefined behavior. If the touch keyboard isn't already running, calling <b>Release</b> could cause tiptsf.dll to be unloaded, because there are no more references to the dll. If this occurs, the state set by the <b>RequireTouchInEditControl</b> method is lost.</div>
<div> </div>
If you need to delay the invocation of the touch keyboard until a later time, like when animations or direct manipulation have completed, use  the <b>IsUIBusy</b> custom UI automation property. For more info, see <a href="/windows/desktop/WinAuto/uiauto-regcustompropseventpatterns">Registering Custom Properties, Events, and Control Patterns</a>.

When you set <b>IsUIBusy</b> to <b>True</b>, the touch keyboard doesn't change visual state based on focus changes within the app. It's still able to change visual state based on overriding user action, like using a physical keyboard or manual dismissal.

When you set <b>IsUIBusy</b> to <b>False</b>, the touch keyboard resumes its default behavior and queries synchronously for the control that  has focus.


The following code shows how to register the <b>IsUIBusy</b> custom UI automation property.


```cpp
/* 03391bea-6681-474b-955c-60f664397ac6 */
DEFINE_GUID(
    GUID_UIBusy, 
    0x03391bea, 0x6681, 0x474b, 0x95, 0x5c, 0x60, 0xf6, 0x64, 0x39, 0x7a, 0xc6);

UIAutomationPropertyInfo customPropertyInfo =
            {
                GUID_UIBusy,
                L"IsUIBusy",
                UIAutomationType_Bool
            };

            CComPtr<IUIAutomationRegistrar> spRegistrar;
            hr = spRegistrar.CoCreateInstance(
                CLSID_CUIAutomationRegistrar, 
                nullptr, 
                CLSCTX_INPROC_SERVER);
            if (SUCCEEDED(hr))
            {
                PATTERNID customPropertyId;
                hr = spRegistrar->RegisterProperty(&customPropertyInfo, &customPropertyId);
            } 

```

## -see-also

<a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelinvocationconfiguration">IInputPanelInvocationConfiguration</a>
