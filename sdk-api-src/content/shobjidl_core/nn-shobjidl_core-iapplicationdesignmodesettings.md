---
UID: NN:shobjidl_core.IApplicationDesignModeSettings
title: IApplicationDesignModeSettings
author: windows-sdk-content
description: Enables development tool applications to dynamically spoof system and user states, such as native display resolution, device scale factor, and application view state, for the purpose of testing Windows Store apps running in design mode for a wide range of form factors without the need for the actual hardware. Also enables testing of changes in normally user-controlled state to test Windows Store apps under a variety of scenarios.
old-location: shell\IApplicationDesignModeSettings.htm
old-project: shell
ms.assetid: D26C9A87-8C29-4029-BF8A-E0566DC2DF2A
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IApplicationDesignModeSettings, IApplicationDesignModeSettings interface [Windows Shell], IApplicationDesignModeSettings interface [Windows Shell],described, shell.IApplicationDesignModeSettings, shobjidl_core/IApplicationDesignModeSettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Twinapi.dll
api_name:
 - IApplicationDesignModeSettings
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Twinapi.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IApplicationDesignModeSettings interface


## -description


Enables development tool applications to dynamically spoof system and user states, such as native display resolution, device scale factor, and application view state, for the purpose of testing Windows Store apps running in design mode for a wide range of form factors without the need for the actual hardware. Also enables testing of changes in normally user-controlled state to test Windows Store apps under a variety of scenarios.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IApplicationDesignModeSettings</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IApplicationDesignModeSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IApplicationDesignModeSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ac42bb8-1c24-4369-8d0d-db3ad4062501">ComputeApplicationSize</a>
</td>
<td align="left" width="63%">
Gets the size of the Windows Store app, based on the current set of spoofed settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49661f00-15bc-48c0-a302-b81bee61180a">IsApplicationViewStateSupported</a>
</td>
<td align="left" width="63%">
Determines whether a particular application view state is supported for specific spoofed display size and scale factor settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37e1845c-a58a-4da3-b259-bbf5bbf5ff6d">SetApplicationViewState</a>
</td>
<td align="left" width="63%">
Sets a spoofed application view state (full-screen landscape, full-screen portrait, filled, or snapped) to be used for a Windows Store app running in design mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc301573-6550-4e21-b82b-7800bbf34ea6">SetNativeDisplaySize</a>
</td>
<td align="left" width="63%">
Sets a spoofed native display size to be used for a Windows Store app running in design mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55b80010-a71e-44c2-8105-e9f5b9a833f5">SetScaleFactor</a>
</td>
<td align="left" width="63%">
Sets a spoofed device scale factor to be used for a Windows Store app running in design mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0B74E779-543F-411F-B6BA-44F00C4D70BE">TriggerEdgeGesture</a>
</td>
<td align="left" width="63%">
Sends a spoofed edge gesture event to the proxy core window on the caller's thread. This gesture toggles the app's app bar, if the app supports one. The caller can specify the type of input that triggered the edge gesture.

</td>
</tr>
</table> 


## -remarks



This interface is acquired by cocreating CLSID_ApplicationDesignModeSettings.

Users will normally follow a usage pattern similar to the following:
            
                

<ol>
<li>Call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> with CLSID_ApplicationDesignModeSettings to create the application design mode settings object on a thread in the Windows Store app process.</li>
<li>Call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the application design mode settings object to obtain an <a href="https://msdn.microsoft.com/8421BFA0-0655-447c-99BB-3D4F049C572D">IInitializeWithWindow</a> object.</li>
<li>Call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method of the <a href="https://msdn.microsoft.com/8421BFA0-0655-447c-99BB-3D4F049C572D">IInitializeWithWindow</a> object, passing in the HWND for the proxy core window. This must be done before any "set" methods are called and will only succeed once per process.</li>
<li>Call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for <b>IApplicationDesignModeSettings</b> and spoof the necessary test state by calling its appropriate methods (<a href="https://msdn.microsoft.com/fc301573-6550-4e21-b82b-7800bbf34ea6">SetNativeDisplaySize</a>, <a href="https://msdn.microsoft.com/55b80010-a71e-44c2-8105-e9f5b9a833f5">SetScaleFactor</a>, etc.). These methods will trigger the appropriate Windows Runtime events to fire for the Windows Store app.</li>
<li>Call the <a href="https://msdn.microsoft.com/1ac42bb8-1c24-4369-8d0d-db3ad4062501">ComputeApplicationSize</a> method to determine the proper size for the app, based on the currently spoofed state. All layout "set" methods must have already been called or this call will fail. The developer tool application is responsible for positioning and sizing the app windows, when appropriate.</li>
</ol>
<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Do not implement this interface; the implementation is supplied with Windows.

<h3><a id="When_to_use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to use</h3>
Use the methods of this interface to test your Windows Store app under various spoofed configurations and scenarios.


#### Examples

This example shows the methods of this interface in use.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IApplicationDesignModeSettings *pDesignModeSettings;

// CoCreate the design mode settings object
HRESULT hr = CoCreateInstance(CLSID_ApplicationDesignModeSettings, nullptr, CLSCTX_INPROC, IID_PPV_ARGS(&amp;pDesignModeSettings));
if (SUCCEEDED(hr))
{
    IInitializeWithWindow *pInitializeWithWindow;
    hr = pDesignModeSettings-&gt;QueryInterface(IID_PPV_ARGS(&amp;pInitializeWithWindow);
    if (SUCCEEDED(hr))
    {
        // Before we spoof any state, we must first initialize the design
        // mode settings object with a proxy core window. Since apps
        // running in design mode don't have an actual core window, we must
        // supply an HWND that can be used as a proxy.
        hr = pInitializeWithWindow-&gt;Initialize(hwndProxyCoreWindow);
        pInitializeWithWindow-&gt;Release();
    }

    if (SUCCEEDED(hr))
    {
        // Verify that our desired spoofed settings are supported.
        SIZE sizeNativeDisplay = {1366, 768};
        SCALE_FACTOR scaleFactor = SCALE_100_PERCENT;
        APPLICATION_VIEW_STATE viewState = AVS_FULLSCREEN_LANDSCAPE;
        BOOL fSupported;
        hr = pDesignModeSettings-&gt;IsApplicationViewStateSupported(viewState,
                                                                  sizeNativeDisplay,
                                                                  scaleFactor,
                                                                  &amp;fSupported);
    }

    if (SUCCEEDED(hr) &amp;&amp; fSupported))
    {
        // Set the spoofed native display size.
        hr = pDesignModeSettings-&gt;SetNativeDisplaySize(sizeNativeDisplay);

        if (SUCCEEDED(hr))
        {
            // Set the spoofed scale factor to 100%.
            hr = pDesignModeSettings-&gt;SetScaleFactor(SCALE_100_PERCENT);
        }

        if (SUCCEEDED(hr))
        {
            // Set the spoofed application view state to full-screen landscape.
            hr = pDesignModeSettings-&gt;SetApplicationViewState(AVS_FULLSCREEN_LANDSCAPE);
        }

        if (SUCCEEDED(hr))
        {
            // Now that all the necessary state has been spoofed, calculate
            // the size that the app should occupy.
            SIZE sizeApplication;
            hr = pDesignModeSettings-&gt;ComputeApplicationSize(&amp;sizeApplication);
        }
    }

    pDesignModeSettings-&gt;Release();
}</pre>
</td>
</tr>
</table></span></div>


