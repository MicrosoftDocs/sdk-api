---
UID: NF:rtscom.IRealTimeStylus3.put_MultiTouchEnabled
title: IRealTimeStylus3::put_MultiTouchEnabled (rtscom.h)
description: Indicates whether the IRealTimeStylus3 object has multitouch input enabled. (Put)
helpviewer_keywords: ["IRealTimeStylus3 interface [Tablet PC]","MultiTouchEnabled property","IRealTimeStylus3.MultiTouchEnabled","IRealTimeStylus3.get_MultiTouchEnabled","IRealTimeStylus3.put_MultiTouchEnabled","IRealTimeStylus3::MultiTouchEnabled","IRealTimeStylus3::get_MultiTouchEnabled","IRealTimeStylus3::put_MultiTouchEnabled","MultiTouchEnabled property [Tablet PC]","MultiTouchEnabled property [Tablet PC]","IRealTimeStylus3 interface","put_MultiTouchEnabled","rtscom/IRealTimeStylus3::MultiTouchEnabled","rtscom/IRealTimeStylus3::get_MultiTouchEnabled","rtscom/IRealTimeStylus3::put_MultiTouchEnabled","tablet.irealtimestylus3_multitouchenabled"]
old-location: tablet\irealtimestylus3_multitouchenabled.htm
tech.root: tablet
ms.assetid: cc573213-a6ed-424b-8513-d5655ba6785a
ms.date: 12/05/2018
ms.keywords: IRealTimeStylus3 interface [Tablet PC],MultiTouchEnabled property, IRealTimeStylus3.MultiTouchEnabled, IRealTimeStylus3.get_MultiTouchEnabled, IRealTimeStylus3.put_MultiTouchEnabled, IRealTimeStylus3::MultiTouchEnabled, IRealTimeStylus3::get_MultiTouchEnabled, IRealTimeStylus3::put_MultiTouchEnabled, MultiTouchEnabled property [Tablet PC], MultiTouchEnabled property [Tablet PC],IRealTimeStylus3 interface, put_MultiTouchEnabled, rtscom/IRealTimeStylus3::MultiTouchEnabled, rtscom/IRealTimeStylus3::get_MultiTouchEnabled, rtscom/IRealTimeStylus3::put_MultiTouchEnabled, tablet.irealtimestylus3_multitouchenabled
req.header: rtscom.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRealTimeStylus3::put_MultiTouchEnabled
 - rtscom/IRealTimeStylus3::put_MultiTouchEnabled
dev_langs:
 - c++
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
---

# IRealTimeStylus3::put_MultiTouchEnabled


## -description

Indicates whether the <a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3">IRealTimeStylus3</a> object has multitouch input enabled.

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

The following example demonstrates how to enable multitouch using the <a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3">RealTimeStylus3</a> interface.


```cpp

CComQIPtr<IRealTimeStylus3> spRealTimeStylus3 = g_spRealTimeStylus;
if(spRealTimeStylus3 == NULL)
{
    return FALSE;
}
HRESULT hr = spRealTimeStylus3->put_MultiTouchEnabled(TRUE);
if(FAILED(hr))
{
    return FALSE;
}
```


The following example shows how to explicitly set the TABLET_ENABLE_MULTITOUCHDATA property on a window.


```cpp
    
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

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3">IRealTimeStylus3</a>
