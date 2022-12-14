---
UID: NN:shobjidl_core.IApplicationDesignModeSettings
title: IApplicationDesignModeSettings (shobjidl_core.h)
description: Enables development tool applications to dynamically spoof system and user states, such as native display resolution, device scale factor, and application view state, for the purpose of testing Windows Store apps running in design mode for a wide range of form factors without the need for the actual hardware. Also enables testing of changes in normally user-controlled state to test Windows Store apps under a variety of scenarios.
helpviewer_keywords: ["IApplicationDesignModeSettings","IApplicationDesignModeSettings interface [Windows Shell]","IApplicationDesignModeSettings interface [Windows Shell]","described","shell.IApplicationDesignModeSettings","shobjidl_core/IApplicationDesignModeSettings"]
old-location: shell\IApplicationDesignModeSettings.htm
tech.root: shell
ms.assetid: D26C9A87-8C29-4029-BF8A-E0566DC2DF2A
ms.date: 12/05/2018
ms.keywords: IApplicationDesignModeSettings, IApplicationDesignModeSettings interface [Windows Shell], IApplicationDesignModeSettings interface [Windows Shell],described, shell.IApplicationDesignModeSettings, shobjidl_core/IApplicationDesignModeSettings
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Twinapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationDesignModeSettings
 - shobjidl_core/IApplicationDesignModeSettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Twinapi.dll
api_name:
 - IApplicationDesignModeSettings
---

# IApplicationDesignModeSettings interface


## -description

Enables development tool applications to dynamically spoof system and user states, such as native display resolution, device scale factor, and application view state, for the purpose of testing Windows Store apps running in design mode for a wide range of form factors without the need for the actual hardware. Also enables testing of changes in normally user-controlled state to test Windows Store apps under a variety of scenarios.

## -inheritance

The <b>IApplicationDesignModeSettings</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IApplicationDesignModeSettings</b> also has these types of members:

## -remarks

This interface is acquired by cocreating CLSID_ApplicationDesignModeSettings.

Users will normally follow a usage pattern similar to the following:
            
                

<ol>
<li>Call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with CLSID_ApplicationDesignModeSettings to create the application design mode settings object on a thread in the Windows Store app process.</li>
<li>Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the application design mode settings object to obtain an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow">IInitializeWithWindow</a> object.</li>
<li>Call the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithwindow-initialize">Initialize</a> method of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow">IInitializeWithWindow</a> object, passing in the HWND for the proxy core window. This must be done before any "set" methods are called, and will succeed only once per process. For a code example, see [Display WinRT UI objects that depend on CoreWindow](/windows/apps/develop/ui-input/display-ui-objects#winui-3-with-c).</li>
<li>Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for <b>IApplicationDesignModeSettings</b> and spoof the necessary test state by calling its appropriate methods (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setnativedisplaysize">SetNativeDisplaySize</a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setscalefactor">SetScaleFactor</a>, etc.). These methods will trigger the appropriate Windows Runtime events to fire for the Windows Store app.</li>
<li>Call the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-computeapplicationsize">ComputeApplicationSize</a> method to determine the proper size for the app, based on the currently spoofed state. All layout "set" methods must have already been called or this call will fail. The developer tool application is responsible for positioning and sizing the app windows, when appropriate.</li>
</ol>
<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Do not implement this interface; the implementation is supplied with Windows.

<h3><a id="When_to_use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to use</h3>
Use the methods of this interface to test your Windows Store app under various spoofed configurations and scenarios.


#### Examples

This example shows the methods of this interface in use.


```cpp

IApplicationDesignModeSettings *pDesignModeSettings;

// CoCreate the design mode settings object
HRESULT hr = CoCreateInstance(CLSID_ApplicationDesignModeSettings, nullptr, CLSCTX_INPROC, IID_PPV_ARGS(&pDesignModeSettings));
if (SUCCEEDED(hr))
{
    IInitializeWithWindow *pInitializeWithWindow;
    hr = pDesignModeSettings->QueryInterface(IID_PPV_ARGS(&pInitializeWithWindow);
    if (SUCCEEDED(hr))
    {
        // Before we spoof any state, we must first initialize the design
        // mode settings object with a proxy core window. Since apps
        // running in design mode don't have an actual core window, we must
        // supply an HWND that can be used as a proxy.
        hr = pInitializeWithWindow->Initialize(hwndProxyCoreWindow);
        pInitializeWithWindow->Release();
    }

    if (SUCCEEDED(hr))
    {
        // Verify that our desired spoofed settings are supported.
        SIZE sizeNativeDisplay = {1366, 768};
        SCALE_FACTOR scaleFactor = SCALE_100_PERCENT;
        APPLICATION_VIEW_STATE viewState = AVS_FULLSCREEN_LANDSCAPE;
        BOOL fSupported;
        hr = pDesignModeSettings->IsApplicationViewStateSupported(viewState,
                                                                  sizeNativeDisplay,
                                                                  scaleFactor,
                                                                  &fSupported);
    }

    if (SUCCEEDED(hr) && fSupported))
    {
        // Set the spoofed native display size.
        hr = pDesignModeSettings->SetNativeDisplaySize(sizeNativeDisplay);

        if (SUCCEEDED(hr))
        {
            // Set the spoofed scale factor to 100%.
            hr = pDesignModeSettings->SetScaleFactor(SCALE_100_PERCENT);
        }

        if (SUCCEEDED(hr))
        {
            // Set the spoofed application view state to full-screen landscape.
            hr = pDesignModeSettings->SetApplicationViewState(AVS_FULLSCREEN_LANDSCAPE);
        }

        if (SUCCEEDED(hr))
        {
            // Now that all the necessary state has been spoofed, calculate
            // the size that the app should occupy.
            SIZE sizeApplication;
            hr = pDesignModeSettings->ComputeApplicationSize(&sizeApplication);
        }
    }

    pDesignModeSettings->Release();
}
```
