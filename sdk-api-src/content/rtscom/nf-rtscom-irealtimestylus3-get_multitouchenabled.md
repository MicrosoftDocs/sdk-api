---
UID: NF:rtscom.IRealTimeStylus3.get_MultiTouchEnabled
title: IRealTimeStylus3::get_MultiTouchEnabled
author: windows-sdk-content
description: Indicates whether the IRealTimeStylus3 object has multitouch input enabled.
old-location: tablet\irealtimestylus3_multitouchenabled.htm
old-project: tablet
ms.assetid: cc573213-a6ed-424b-8513-d5655ba6785a
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IRealTimeStylus3 interface [Tablet PC],MultiTouchEnabled property, IRealTimeStylus3.MultiTouchEnabled, IRealTimeStylus3.get_MultiTouchEnabled, IRealTimeStylus3.put_MultiTouchEnabled, IRealTimeStylus3::MultiTouchEnabled, IRealTimeStylus3::get_MultiTouchEnabled, IRealTimeStylus3::put_MultiTouchEnabled, MultiTouchEnabled property [Tablet PC], MultiTouchEnabled property [Tablet PC],IRealTimeStylus3 interface, get_MultiTouchEnabled, rtscom/IRealTimeStylus3::MultiTouchEnabled, rtscom/IRealTimeStylus3::get_MultiTouchEnabled, rtscom/IRealTimeStylus3::put_MultiTouchEnabled, tablet.irealtimestylus3_multitouchenabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rtscom.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rtscom.h
api_name:
 - IRealTimeStylus3.MultiTouchEnabled
 - IRealTimeStylus3.get_MultiTouchEnabled
 - IRealTimeStylus3.put_MultiTouchEnabled
 - IRealTimeStylus3.get_MultiTouchEnabled
 - IRealTimeStylus3.put_MultiTouchEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

