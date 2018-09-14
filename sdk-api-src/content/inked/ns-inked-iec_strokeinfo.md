---
UID: NS:inked.IEC_STROKEINFO
title: IEC_STROKEINFO
author: windows-sdk-content
description: Contains information about a Stroke event.
old-location: tablet\iec_strokeinfo__win32_only_.htm
tech.root: tablet
ms.assetid: 12486d28-eba2-4ef6-802e-be7155de6edd
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 12486d28-eba2-4ef6-802e-be7155de6edd, IEC_STROKEINFO, IEC_STROKEINFO (Win32 Only), IEC_STROKEINFO (Win32 Only) structure [Tablet PC], inked/IEC_STROKEINFO, structure [Tablet PC], tablet.iec_strokeinfo__win32_only_
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - inked.h
api_name:
 - IEC_STROKEINFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEC_STROKEINFO structure


## -description



Contains information about a <a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke</a> event.




## -struct-fields




### -field nmhdr

Specifies the NMHDR structure that contains standard information about the WM_NOTIFY message. The NMHDR structure contains the handle and identifier of the control that is sending the message and the notification code, which in this case is <a href="https://msdn.microsoft.com/26023012-9ab1-4bd9-beff-41587bc74f5e">IECN_STROKE</a>. The format of the NMHDR structure is:

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

The <a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor</a> object that was used to create the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object.


### -field Stroke

The <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object that was created.


## -see-also




<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>



<a href="https://msdn.microsoft.com/fac5104d-d0da-40b1-a4a6-00a34718d09f">Stroke Event [InkEdit Control]</a>



<a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>
 

 

