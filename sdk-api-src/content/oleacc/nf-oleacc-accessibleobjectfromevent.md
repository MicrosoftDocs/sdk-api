---
UID: NF:oleacc.AccessibleObjectFromEvent
title: AccessibleObjectFromEvent function
author: windows-sdk-content
description: Retrieves the address of the IAccessible interface for the object that generated the event that is currently being processed by the client's event hook function.
old-location: winauto\accessibleobjectfromevent.htm
old-project: WinAuto
ms.assetid: d453c163-3918-4a1c-9636-16816227a295
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: AccessibleObjectFromEvent, AccessibleObjectFromEvent function [Windows Accessibility], _msaa_AccessibleObjectFromEvent, msaa.accessibleobjectfromevent, oleacc/AccessibleObjectFromEvent, winauto.accessibleobjectfromevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - AccessibleObjectFromEvent
product: Windows
targetos: Windows
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# AccessibleObjectFromEvent function


## -description


Retrieves the address of the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface for the object that generated the event that is currently being processed by the client's event hook function.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Specifies the window handle of the window that generated the event. This value must be the window handle that is sent to the event hook function.


### -param dwId

TBD


### -param dwChildId

TBD


### -param ppacc [out]

Type: <b>IAccessible**</b>

Address of a pointer variable that receives the address of an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface. The interface is either for the object that generated the event, or for the parent of the element that generated the event.


### -param pvarChild [out]

Type: <b>VARIANT*</b>

Address of a <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT structure</a> that specifies the child ID that can be used to access information about the UI element.


#### - dwChildID [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies whether the event was triggered by an object or one of its child elements. If the object triggered the event, <i>dwChildID</i> is CHILDID_SELF. If a child element triggered the event, <i>dwChildID</i> is the element's child ID. This value must be the child ID that is sent to the event hook function.


#### - dwObjectID [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the object ID of the object that generated the event. This value must be the object ID that is sent to the event hook function.


## -returns



Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns one of the following or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is not valid.

</td>
</tr>
</table>
 




## -remarks



Clients call this function within an event hook function to obtain an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface pointer to either the object that generated the event or to the parent of the element that generated the event. The parameters sent to the <a href="https://msdn.microsoft.com/5fe3cacc-4563-43da-960d-729d3fe4ff70">WinEventProc</a> callback function must be used for this function's <i>hwnd</i>, <i>dwObjectID</i>, and <i>dwChildID</i> parameters.

This function retrieves the lowest-level accessible object in the object hierarchy that is associated with an event. If the element that generated the event is not an accessible object (that is, does not support <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>), then the function retrieves the <b>IAccessible</b> interface of the parent object. The parent object must provide information about the child element through the <b>IAccessible</b> interface.

As with other <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="https://msdn.microsoft.com/408bfa47-fda0-4a25-89c1-da41d967ad61">Receiving Errors for IAccessible Interface Pointers</a>.

This function fails if called in response to <a href="https://www.bing.com/search?q=EVENT_OBJECT_CREATE">EVENT_OBJECT_CREATE</a> because the object is not fully initialized. Similarly, clients should not call this in response to <a href="https://www.bing.com/search?q=EVENT_OBJECT_DESTROY">EVENT_OBJECT_DESTROY</a> because the object is no longer available and cannot respond. Clients watch for <a href="https://www.bing.com/search?q=EVENT_OBJECT_SHOW">EVENT_OBJECT_SHOW</a> and <a href="https://www.bing.com/search?q=EVENT_OBJECT_HIDE">EVENT_OBJECT_HIDE</a> events rather than for <b>EVENT_OBJECT_CREATE</b> and <b>EVENT_OBJECT_DESTROY</b>.


#### Examples

The following example code shows this method being called in a <a href="https://msdn.microsoft.com/5fe3cacc-4563-43da-960d-729d3fe4ff70">WinEventProc</a> event handler.



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
void CALLBACK HandleWinEvent(HWINEVENTHOOK hook, DWORD event, HWND hwnd, 
                             LONG idObject, LONG idChild, 
                             DWORD dwEventThread, DWORD dwmsEventTime)
{
    IAccessible* pAcc = NULL;
    VARIANT varChild;
    HRESULT hr = AccessibleObjectFromEvent(hwnd, idObject, idChild, &amp;pAcc, &amp;varChild);  
    if ((hr == S_OK) &amp;&amp; (pAcc != NULL))
    {
        // Do something with the accessible object, then release it.        
        // ... 
        pAcc-&gt;Release();
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b781b74f-5c36-4a65-a9b1-ecf7f8e5b531">AccessibleObjectFromPoint</a>



<a href="https://msdn.microsoft.com/297ac50f-2a58-477b-ba57-5d1416c191b3">AccessibleObjectFromWindow</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>



<a href="https://msdn.microsoft.com/5fe3cacc-4563-43da-960d-729d3fe4ff70">WinEventProc</a>
 

 

