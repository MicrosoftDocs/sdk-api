---
UID: NS:inked.IEC_RECOGNITIONRESULTINFO
title: IEC_RECOGNITIONRESULTINFO
author: windows-driver-content
description: Contains information about an IInkRecognitionResult Interface object.
old-location: tablet\iec_recognitionresultinfo__win32_only_.htm
old-project: tablet
ms.assetid: a17dd2e4-0649-4cfc-aab3-c032710480a1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IEC_RECOGNITIONRESULTINFO, IEC_RECOGNITIONRESULTINFO (Win32 Only), IEC_RECOGNITIONRESULTINFO (Win32 Only) structure [Tablet PC], a17dd2e4-0649-4cfc-aab3-c032710480a1, inked/IEC_RECOGNITIONRESULTINFO, tablet.iec_recognitionresultinfo__win32_only_
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	inked.h
api_name:
-	IEC_RECOGNITIONRESULTINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IEC_RECOGNITIONRESULTINFO structure


## -description



Contains information about an <a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult Interface</a> object.




## -struct-fields




### -field nmhdr

 The NMHDR structure that contains standard information about the WM_NOTIFY message. The NMHDR structure contains the handle and identifier of the control that is sending the message and the notification code, which in this case is <a href="https://msdn.microsoft.com/26023012-9ab1-4bd9-beff-41587bc74f5e">IECN_RECOGNITIONRESULT</a>. The format of the NMHDR structure is:

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

### -field RecognitionResult

The <a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult</a> object that contains recognition results.


## -see-also




<a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult Interface</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>



<a href="https://msdn.microsoft.com/09618be0-fe49-494f-940f-79ff8352097e">RecognitionResult Event</a>



<a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>
 

 

