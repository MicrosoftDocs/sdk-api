---
UID: NS:inked.IEC_GESTUREINFO
title: IEC_GESTUREINFO
author: windows-sdk-content
description: Contains information about a specific gesture.
old-location: tablet\iec_gestureinfo__win32_only_.htm
old-project: tablet
ms.assetid: f932508b-44d3-4605-97a7-bb6eed248939
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IEC_GESTUREINFO, IEC_GESTUREINFO (Win32 Only), IEC_GESTUREINFO (Win32 Only) structure [Tablet PC], f932508b-44d3-4605-97a7-bb6eed248939, inked/IEC_GESTUREINFO, tablet.iec_gestureinfo__win32_only_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: inked.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - inked.h
api_name:
 - IEC_GESTUREINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IEC_GESTUREINFO structure


## -description



Contains information about a specific gesture.




## -struct-fields




### -field nmhdr

The NMHDR structure that contains standard information about the WM_NOTIFY message. The NMHDR structure contains the handle and identifier of the control that is sending the message and the notification code, which in this case is <a href="https://msdn.microsoft.com/26023012-9ab1-4bd9-beff-41587bc74f5e">IECN_GESTURE</a>. The format of the NMHDR structure is:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef struct tagNMHDR {
      HWND hwndFrom;
      UINT idFrom;
      UINT code;
  } NMHDR;</pre>
</td>
</tr>
</table></span></div>

### -field Cursor

The <a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor</a> object that was used to create the gesture.


### -field Strokes

The <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that makes up the gesture.


### -field Gestures

An array of <a href="https://msdn.microsoft.com/87a1db34-371e-4c02-a470-55f35dfbf4ab">IInkGesture</a> objects, in order of confidence. For more information about this member, see the <a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture</a> event.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


## -see-also




<a href="https://msdn.microsoft.com/736715f4-c610-42cc-9fbb-c2b579da69e5">Gesture Event [InkEdit Control]</a>



<a href="https://msdn.microsoft.com/87a1db34-371e-4c02-a470-55f35dfbf4ab">IInkGesture Interface</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>



<a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>
 

 

