---
UID: NF:shobjidl.IAccessibilityDockingServiceCallback.Undocked
title: IAccessibilityDockingServiceCallback::Undocked
author: windows-sdk-content
description: Called when the accessibility window has been undocked, giving the app the chance to redock.
old-location: shell\IAccessibilityDockingServiceCallback_Undocked.htm
tech.root: shell
ms.assetid: AFD60F5B-3017-49a2-8AFC-8309D11B3ACA
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAccessibilityDockingServiceCallback interface [Windows Shell],Undocked method, IAccessibilityDockingServiceCallback.Undocked, IAccessibilityDockingServiceCallback::Undocked, Undocked, Undocked method [Windows Shell], Undocked method [Windows Shell],IAccessibilityDockingServiceCallback interface, shell.IAccessibilityDockingServiceCallback_Undocked, shobjidl/IAccessibilityDockingServiceCallback::Undocked
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IAccessibilityDockingServiceCallback.Undocked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibilityDockingServiceCallback::Undocked


## -description


Called when the accessibility window has been undocked, giving the app the chance to redock.


## -parameters




### -param undockReason [in]

Type: <b>UNDOCK_REASON</b>

One of the enumeration values that explains why the accessibility app window was undocked.


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.




## -remarks



This method informs the app why it was undocked so that it can take an appropriate action. For example, when you react to a resolution change, it might not be necessary to add the adornments of an undocked window because you might want to immediately redock.

When an accessibility app window becomes undocked due to a system event, the system will not automatically attempt to restore it to its previous location. It is safe to perform a redock in this callback method.

After the app has received this <b>Undocked</b> callback, it will not receive any subsequent callbacks unless it has successfully redocked its window.


#### Examples

The following shows an example implementation of this method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
class CAccessibilityApplicationWindow : public IAccessibilityDockingServiceCallback
{
    // ...

    HRESULT Undocked(_In_ UNDOCK_REASON undockReason);
    {
        // This sample only reacts to a resolution change event
        // On monitor disconnect, this will not attempt to request a redock
        if (undockReason == RESOLUTION_CHANGE) 
        {
            _ReRequestDock();
        } 
        return S_OK;
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/E357E47C-5A29-4b92-AD26-E604E501B7D6">IAccessibilityDockingServiceCallback</a>
 

 

