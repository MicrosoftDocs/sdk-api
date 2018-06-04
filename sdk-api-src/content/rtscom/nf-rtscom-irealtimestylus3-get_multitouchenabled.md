---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IRealTimeStylus3::get_MultiTouchEnabled


## -description


Indicates whether the <a href="https://msdn.microsoft.com/93eabb45-0b0e-495f-9b64-43ad8060b958">IRealTimeStylus3</a> object has multitouch input enabled.

This property is read/write.


## -parameters


## -remarks




      The following table lists the defined opt-in options for multitouch.


<table>
<tr>
<th>Name</th>
<th>Description</th>
<th>Value</th>
</tr>
<tr>
<td>TABLET_ENABLE_MULTITOUCHDATA</td>
<td>Indicates opt-in for multitouch data.</td>
<td>0x01000000</td>
</tr>
</table>
 


#### Examples

The following example demonstrates how to enable multitouch using the <a href="https://msdn.microsoft.com/93eabb45-0b0e-495f-9b64-43ad8060b958">RealTimeStylus3</a> interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
CComQIPtr&lt;IRealTimeStylus3&gt; spRealTimeStylus3 = g_spRealTimeStylus;
if(spRealTimeStylus3 == NULL)
{
    return FALSE;
}
HRESULT hr = spRealTimeStylus3-&gt;put_MultiTouchEnabled(TRUE);
if(FAILED(hr))
{
    return FALSE;
}</pre>
</td>
</tr>
</table></span></div>
The following example shows how to explicitly set the TABLET_ENABLE_MULTITOUCHDATA property on a window.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    
    //Set the window property
    ATOM m_atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);
    m_dwProperty = TABLET_ENABLE_MULTITOUCHDATA;
    ::SetProp(m_hwnd, (LPTSTR)m_atomPenService, (HANDLE)m_dwProperty);
     
    //A Window Property takes effect on the down action of the 1st finger.

    //process the LRESULT from WinProc:

    //A custom LRESULT CALLBACK
    GestureTest::WindowProcedure(      
      HWND hwnd,
      UINT uMsg,
      WPARAM wParam,
      LPARAM lParam)
    {
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        return TABLET_ENABLE_MULTITOUCHDATA;
    }    
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/93eabb45-0b0e-495f-9b64-43ad8060b958">IRealTimeStylus3</a>
 

 

