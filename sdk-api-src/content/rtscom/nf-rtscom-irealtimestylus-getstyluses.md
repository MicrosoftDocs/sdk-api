---
UID: NF:rtscom.IRealTimeStylus.GetStyluses
title: IRealTimeStylus::GetStyluses
author: windows-sdk-content
description: Retrieves the collection of styluses the RealTimeStylus Class object has encountered.
old-location: tablet\irealtimestylus_getstyluses.htm
old-project: tablet
ms.assetid: 1e838591-ce9e-4f3f-9b5e-b8414faac6ba
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: 1e838591-ce9e-4f3f-9b5e-b8414faac6ba, GetStyluses, GetStyluses method [Tablet PC], GetStyluses method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetStyluses method, IRealTimeStylus.GetStyluses, IRealTimeStylus::GetStyluses, rtscom/IRealTimeStylus::GetStyluses, tablet.irealtimestylus_getstyluses
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rtscom.h
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
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus.GetStyluses
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IRealTimeStylus::GetStyluses


## -description



Retrieves the collection of styluses the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object has encountered.




## -parameters




### -param ppiInkCursors [out, retval]

When this method returns, contains a pointer to the collection of styluses the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object has encountered.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> collection includes the styluses for which a tablet context has been created. The collection does not include all styluses available in the system in the stylus collection.

If no stylus object has been detected on the tablet objects associated with the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object, this method returns an empty array.

This method cannot be called unless it the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object is connected and enabled <b>RealTimeStylus Class</b>.

<div class="alert"><b>Note</b>  This method can be called if <a href="https://msdn.microsoft.com/e96e27d7-b453-49a7-b684-b3dd5f94c378">IRealTimeStylus::Enabled Property</a> returns false as long as the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object has not finished processing data in the queue. This method can be called until the last asynchronous plug-in receives <a href="https://msdn.microsoft.com/62425c21-62fb-4a29-b024-8d5dc237b430">IStylusPlugin::RealTimeStylusDisabled Method</a>.</div>
<div> </div>

#### Examples

The following C++ example code gets an array of the Stylus objects that the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object has encountered since it was last enabled. It then iterates through the array reporting the ID of each stylus in debug output.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IInkCursors *piInkCursors;

if (SUCCEEDED(g_pRealTimeStylus-&gt;GetStyluses(&amp;piInkCursors)))
{
    long lCursorCount;
    
    if (SUCCEEDED(piInkCursors-&gt;get_Count(&amp;lCursorCount)))
    {
        for (long l = 0; l &lt; lCursorCount; l++)
        {
            LONG sid;
            IInkCursor *piInkCursor;
            IInkCursor *piInkCursorForId;

            piInkCursors-&gt;Item(l, &amp;piInkCursor);
            piInkCursor-&gt;get_Id(&amp;sid);

            if (SUCCEEDED(g_pRealTimeStylus-&gt;GetStylusForId((STYLUS_ID)sid, &amp;piInkCursorForId)))
            {
                TRACE("Got stylus with ID %d\n", sid);
            }
        }
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/16218bd3-9e92-407b-99b1-155d4387641e">IRealTimeStylus::GetStylusForId Method</a>



<b>RealTimeStylus Class</b>
 

 

