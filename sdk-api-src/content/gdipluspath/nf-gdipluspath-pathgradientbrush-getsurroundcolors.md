---
UID: NF:gdipluspath.PathGradientBrush.GetSurroundColors
title: PathGradientBrush::GetSurroundColors
author: windows-sdk-content
description: The PathGradientBrush::GetSurroundColors method gets the surround colors currently specified for this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetSurroundColors_colors_count_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\getsurroundcolors.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetSurroundColors, GetSurroundColors method [GDI+], GetSurroundColors method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetSurroundColors method, PathGradientBrush.GetSurroundColors, PathGradientBrush::GetSurroundColors, _gdiplus_CLASS_PathGradientBrush_GetSurroundColors_colors_count_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetSurroundColors_colors_count_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WmfPlaceableFileHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	PathGradientBrush.GetSurroundColors
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# PathGradientBrush::GetSurroundColors


## -description


The <b>PathGradientBrush::GetSurroundColors</b> method gets the surround colors currently specified for this path gradient brush.


## -parameters




### -param colors [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>*</b>

Pointer to an array that receives the surround colors. 


### -param count [in, out]

Type: <b>INT*</b>

Pointer to an integer that, on input, specifies the number of colors requested. If the method succeeds, this parameter, on output, receives the number of colors retrieved. If the method fails, this parameter does not receive a value. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



A path gradient brush has a boundary path and a center point. The center point is set to a single color, but you can specify different colors for several points on the boundary. For example, suppose you specify red for the center color, and you specify blue, green, and yellow for distinct points on the boundary. Then as you move along the boundary, the color will change gradually from blue to green to yellow and back to blue. As you move along a straight line from any point on the boundary to the center point, the color will change from that boundary point's color to red.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>
 object based on a triangular path that is defined by an array of three points. The code calls the <a href="https://msdn.microsoft.com/80c24a7a-feed-40a3-bbdf-ff971e8aac68">PathGradientBrush::SetSurroundColors</a> method of the 
						<b>PathGradientBrush</b>
 object to specify a color for each of the points that define the triangle. The <a href="https://msdn.microsoft.com/c401fbbb-903c-427f-b4e3-b0add504c584">PathGradientBrush::GetSurroundColorCount</a> method determines the current number of surround colors (the colors specified for the brush's boundary path). Next, the code allocates a buffer large enough to receive the array of surround colors and calls <b>PathGradientBrush::GetSurroundColors</b> to fill that buffer. Finally the code fills a small square with each of the brush's surround colors.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetSurColors(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path gradient brush and set its surround colors.
   Point pts[] = {
      Point(20, 20), 
      Point(100, 20), 
      Point(100, 100)};

   Color cols[] = {
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 255, 0),  // green
      Color(255, 0, 0, 0)};   // black

   INT count = 3;
   PathGradientBrush pthGrBrush(pts, 3);
   pthGrBrush.SetSurroundColors(cols, &amp;count);
   
   // Obtain information about the path gradient brush.
   INT colorCount = pthGrBrush.GetSurroundColorCount();
   Color* colors = new Color[colorCount];
   pthGrBrush.GetSurroundColors(colors, &amp;colorCount);

   // Fill a small square with each of the surround colors.
   SolidBrush solidBrush(Color(255, 255, 255, 255));

   for(INT j = 0; j &lt; colorCount; ++j)
   {
      solidBrush.SetColor(colors[j]);
      graphics.FillRectangle(&amp;solidBrush, 15*j, 0, 10, 10);
   }

   delete [] colors;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/c401fbbb-903c-427f-b4e3-b0add504c584">PathGradientBrush::GetSurroundColorCount</a>



<a href="https://msdn.microsoft.com/80c24a7a-feed-40a3-bbdf-ff971e8aac68">PathGradientBrush::SetSurroundColors</a>
 

 

