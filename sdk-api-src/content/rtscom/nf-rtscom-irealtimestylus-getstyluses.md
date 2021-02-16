---
UID: NF:rtscom.IRealTimeStylus.GetStyluses
title: IRealTimeStylus::GetStyluses (rtscom.h)
description: Retrieves the collection of styluses the RealTimeStylus Class object has encountered.
helpviewer_keywords: ["1e838591-ce9e-4f3f-9b5e-b8414faac6ba","GetStyluses","GetStyluses method [Tablet PC]","GetStyluses method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","GetStyluses method","IRealTimeStylus.GetStyluses","IRealTimeStylus::GetStyluses","rtscom/IRealTimeStylus::GetStyluses","tablet.irealtimestylus_getstyluses"]
old-location: tablet\irealtimestylus_getstyluses.htm
tech.root: tablet
ms.assetid: 1e838591-ce9e-4f3f-9b5e-b8414faac6ba
ms.date: 12/05/2018
ms.keywords: 1e838591-ce9e-4f3f-9b5e-b8414faac6ba, GetStyluses, GetStyluses method [Tablet PC], GetStyluses method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetStyluses method, IRealTimeStylus.GetStyluses, IRealTimeStylus::GetStyluses, rtscom/IRealTimeStylus::GetStyluses, tablet.irealtimestylus_getstyluses
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRealTimeStylus::GetStyluses
 - rtscom/IRealTimeStylus::GetStyluses
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus.GetStyluses
---

# IRealTimeStylus::GetStyluses


## -description

Retrieves the collection of styluses the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object has encountered.

## -parameters

### -param ppiInkCursors [out, retval]

When this method returns, contains a pointer to the collection of styluses the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object has encountered.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> collection includes the styluses for which a tablet context has been created. The collection does not include all styluses available in the system in the stylus collection.

If no stylus object has been detected on the tablet objects associated with the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object, this method returns an empty array.

This method cannot be called unless it the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object is connected and enabled <b>RealTimeStylus Class</b>.

<div class="alert"><b>Note</b>  This method can be called if <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-get_enabled">IRealTimeStylus::Enabled Property</a> returns false as long as the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object has not finished processing data in the queue. This method can be called until the last asynchronous plug-in receives <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-realtimestylusdisabled">IStylusPlugin::RealTimeStylusDisabled Method</a>.</div>
<div> </div>

#### Examples

The following C++ example code gets an array of the Stylus objects that the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object has encountered since it was last enabled. It then iterates through the array reporting the ID of each stylus in debug output.


```cpp
IInkCursors *piInkCursors;

if (SUCCEEDED(g_pRealTimeStylus->GetStyluses(&piInkCursors)))
{
    long lCursorCount;
    
    if (SUCCEEDED(piInkCursors->get_Count(&lCursorCount)))
    {
        for (long l = 0; l < lCursorCount; l++)
        {
            LONG sid;
            IInkCursor *piInkCursor;
            IInkCursor *piInkCursorForId;

            piInkCursors->Item(l, &piInkCursor);
            piInkCursor->get_Id(&sid);

            if (SUCCEEDED(g_pRealTimeStylus->GetStylusForId((STYLUS_ID)sid, &piInkCursorForId)))
            {
                TRACE("Got stylus with ID %d\n", sid);
            }
        }
    }
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstylusforid">IRealTimeStylus::GetStylusForId Method</a>



<b>RealTimeStylus Class</b>