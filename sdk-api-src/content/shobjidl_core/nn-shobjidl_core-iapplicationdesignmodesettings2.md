---
UID: NN:shobjidl_core.IApplicationDesignModeSettings2
title: IApplicationDesignModeSettings2
author: windows-driver-content
description: Enables development tool applications to dynamically control system and user states, such as native display resolution, device scale factor, and application view layout, reported to Windows Store apps for the purpose of testing Windows Store apps running in design mode for a wide range of form factors without the need for the actual hardware. Also enables testing of changes in normally user-controlled state to test Windows Store apps under a variety of scenarios.
old-location: shell\IApplicationDesignModeSettings2.htm
old-project: shell
ms.assetid: 1F630AFF-3C73-461C-AE41-D597F6FF42D8
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IApplicationDesignModeSettings2, IApplicationDesignModeSettings2 interface [Windows Shell], IApplicationDesignModeSettings2 interface [Windows Shell],described, shell.IApplicationDesignModeSettings2, shobjidl_core/IApplicationDesignModeSettings2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	twinapi.dll
api_name:
-	IApplicationDesignModeSettings2
product: Windows
targetos: Windows
req.lib: Twinapi.lib
req.dll: Twinapi.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IApplicationDesignModeSettings2 interface


## -description


Enables development tool applications to dynamically control system and user states, such as native display resolution, device scale factor, and application view layout, reported to Windows Store apps for the purpose of testing Windows Store apps running in design mode for a wide range of form factors without the need for the actual hardware. Also enables testing of changes in normally user-controlled state to test Windows Store apps under a variety of scenarios.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IApplicationDesignModeSettings2</b> interface inherits from <a href="https://msdn.microsoft.com/D26C9A87-8C29-4029-BF8A-E0566DC2DF2A">IApplicationDesignModeSettings</a>. <b>IApplicationDesignModeSettings2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IApplicationDesignModeSettings2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7DFAFE5A-8F19-471C-9B09-43645F26F156">GetApplicationSizeBounds</a>
</td>
<td align="left" width="63%">
This methods retrieves the size bounds supported by the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D6DF8432-7D37-4D39-9E08-2F5B874A0BCB">GetApplicationViewOrientation</a>
</td>
<td align="left" width="63%">
Gets the orientation of the application design mode window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD8B2436-1ADD-4371-AEB4-27EBDEC5BA04">SetAdjacentDisplayEdges</a>
</td>
<td align="left" width="63%">
Sets whether the application window will be  adjacent to the edge of the emulated display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6132E0B9-E2B9-4768-909A-9D93A3F3A11C">SetApplicationViewMinWidth</a>
</td>
<td align="left" width="63%">
Sets the desired minimum width of the application design mode window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FCD2FDFD-1058-45D6-B9D5-A4B845CF80AA">SetApplicationViewOrientation</a>
</td>
<td align="left" width="63%">
Sets the window orientation used for the design mode window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5BFBB0E4-2448-44B1-B2F3-68AB8392C3A4">SetIsOnLockScreen</a>
</td>
<td align="left" width="63%">
This method determines whether or not the application, in design mode, can display information on the Windows 8 lock screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9473724C-3FD2-48D0-BCFA-EA148F0C4569">SetNativeDisplayOrientation</a>
</td>
<td align="left" width="63%">
Sets the orientation of the emulated display for the design mode window.

</td>
</tr>
</table> 


## -remarks



This interface is acquired by cocreating CLSID_ApplicationDesignModeSettings. It is an extension of the original <a href="https://msdn.microsoft.com/D26C9A87-8C29-4029-BF8A-E0566DC2DF2A">IApplicationDesignModeSettings</a> interface.


#### Examples

In this example, Visual Studio is launching an application in design mode that has overridden the minimum width on a display of size 1366x768. It is then enabling a slider control that allows the user to dynamically change the applications width. To do this, it needs to use the new <a href="https://msdn.microsoft.com/6132E0B9-E2B9-4768-909A-9D93A3F3A11C">SetApplicationViewMinWidth</a> and <a href="https://msdn.microsoft.com/7DFAFE5A-8F19-471C-9B09-43645F26F156">GetApplicationSizeBounds</a>APIs to compute the minimum and maximum sizes allowed for this type of application.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ComPtr&lt;IApplicationDesignModeSettings&gt; spDesignModeSettings;

// CoCreate the design mode settings object
HRESULT hr = CoCreateInstance(CLSID_ApplicationDesignModeSettings, nullptr, CLSCTX_INPROC, IID_PPV_ARGS(&amp;spDesignModeSettings));
if (SUCCEEDED(hr))
{
    ComPtr&lt;IInitializeWithWindow&gt; spInitializeWithWindow;
    hr = pDesignModeSettings-&gt;QueryInterface(IID_PPV_ARGS(&amp;spInitializeWithWindow);
    if (SUCCEEDED(hr))
    {
        // Before we set any design mode state, we must first initialize the
        // design mode settings object with a proxy core window. Since apps
        // running in design mode don't have an actual core window, we must
        // supply an HWND that can be used as a proxy.
        hr = spInitializeWithWindow-&gt;Initialize(hwndProxyCoreWindow);
    }

    if (SUCCEEDED(hr))
    {
        // Set the native display size to 1366x768
        SIZE sizeDisplay = {1366, 768};
        hr = spDesignModeSettings-&gt;SetNativeDisplaySize(sizeDisplay);
        if (SUCCEEDED(hr))
        {
            // Set the native display orientation to landscape
            hr = spDesignModeSettings-&gt;SetNativeDisplayOrientation(NDO_LANDSCAPE);
            if (SUCCEEDED(hr))
            {
                // Set the scale factor to 100%
                DEVICE_SCALE_FACTOR scaleFactor = SCALE_100_PERCENT;
                hr = spDesignModeSettings-&gt;SetScaleFactor(scaleFactor);
            }
        }
    }

    if (SUCCEEDED(hr))
    {

        // Override the app’s minimum width
        hr = spDesignModeSettings-&gt;SetApplicationViewMinWidth(AVMW_320);
        if (SUCCEEDED(hr))
        {
            SIZE sizeAppMin;
            SIZE sizeAppMax;
            hr = spDesignModeSettings-&gt;GetApplicationSizeBounds(&amp;sizeAppMin, &amp;sizeAppMax);
            if (SUCCEEDED(hr))
            {
                // Push the min and max size to the slider control,
                // to update the values that it maps to
                …

                // Start by sizing the app to its min bound, so compute the                         
                // resulting view orientation
                APPLICATION_VIEW_ORIENTATION viewOrientation;
                hr = spDesignModeSettings-&gt;GetApplicationViewOrientation(sizeAppMin, &amp;viewOrientation);
                if (SUCCEEDED(hr))
                {
                    // Set the app view orientation
                    hr = spDesignModeSettings-&gt;SetApplicationViewOrientation(viewOrientation);
                }
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        // Set the adjacent display edges so that the app is touching just the left edge of the screen
        hr = spDesignModeSettings-&gt;SetAdjacentDisplayEdges(ADE_LEFT);
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/D26C9A87-8C29-4029-BF8A-E0566DC2DF2A">IApplicationDesignModeSettings</a>
 

 

